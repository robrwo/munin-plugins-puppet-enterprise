# Munin Plugins for Puppet Enterprise

This repository contains Munin Plugins that work with Puppet
Enterprise 3.

## Requirements

The [POSIX::strptime](https://metacpan.org/pod/POSIX::strptime)
module, which on Debian Wheezy is the package
`libposix-strptime-perl`.

## Installation Instructions

```sh
git clone https://github.com/robrwo/munin-plugins-puppet-enterprise.git
cd munin-plugins-puppet-enterprise

sudo mkdir -p /usr/local/share/munin/plugins
sudo cp plugins/puppet_agent !$
sudo chmod +x /usr/local/share/munin/plugins/puppet_agent

sudo ln -s /usr/local/share/munin/plugins/puppet_agent \
  /etc/munin/plugins/puppet_agent

sudo ln -s /usr/local/share/munin/plugins/puppet_agent \
  /etc/munin/plugins/puppet_agent_count

sudo cp plugin-conf.d/puppet_agent /etc/munin/plugin-conf.d/puppet_agent

sudo service munin-node restart
```

## Acknowledgements

- Foxtons, Ltd.

## License

Copyright (c) 2014, Robert Rothenberg <rrwo@cpan.org>

This program is free software; you can redistribute it and/or modify
it under the terms of the the Artistic License (2.0). You may obtain a
copy of the full license at:

http://www.perlfoundation.org/artistic_license_2_0

Any use, modification, and distribution of the Standard or Modified
Versions is governed by this Artistic License. By using, modifying or
distributing the Package, you accept this license. Do not use, modify,
or distribute the Package, if you do not accept this license.

If your Modified Version has been derived from a Modified Version made
by someone other than you, you are nevertheless required to ensure
that your Modified Version complies with the requirements of this
license.

This license does not grant you the right to use any trademark,
service mark, tradename, or logo of the Copyright Holder.

This license includes the non-exclusive, worldwide, free-of-charge
patent license to make, have made, use, offer to sell, sell, import
and otherwise transfer the Package with respect to any patent claims
licensable by the Copyright Holder that are necessarily infringed by
the Package. If you institute patent litigation (including a
cross-claim or counterclaim) against any party alleging that the
Package constitutes direct or contributory patent infringement, then
this Artistic License to you shall terminate on the date that such
litigation is filed.

Disclaimer of Warranty: THE PACKAGE IS PROVIDED BY THE COPYRIGHT
HOLDER AND CONTRIBUTORS "AS IS' AND WITHOUT ANY EXPRESS OR IMPLIED
WARRANTIES. THE IMPLIED WARRANTIES OF MERCHANTABILITY, FITNESS FOR A
PARTICULAR PURPOSE, OR NON-INFRINGEMENT ARE DISCLAIMED TO THE EXTENT
PERMITTED BY YOUR LOCAL LAW. UNLESS REQUIRED BY LAW, NO COPYRIGHT
HOLDER OR CONTRIBUTOR WILL BE LIABLE FOR ANY DIRECT, INDIRECT,
INCIDENTAL, OR CONSEQUENTIAL DAMAGES ARISING IN ANY WAY OUT OF THE USE
OF THE PACKAGE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
