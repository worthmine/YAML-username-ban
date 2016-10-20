# YAML-username-ban

## in perl
```
use YAML::XS qw( LoadFile );
my $y = LoadFile( './common/static/ban.yaml' );
my @ban = @{ $y->{'ban'} };
 die 'そのユニークユーザーIDはシステムにより予約されています。 username=' . $param{'username'}
if $param{'username'} and grep{ lc( $param{'username'} ) eq lc($_) } @ban;
```
