pcap-diff
=========

Diff two or more pcap files and write a pcap file with different packets as result


Requirements
============

Python 2.7
Scapy (pip install scapy)


Example usages
==============

Diff client.dump and server.dump but ignore different packets on client side

.. code-block:: bash

  pcap_diff.py -i client.dump -i server.dump -o diff.pcap -l

Show all differences but ignore all mac addresses 

.. code-block:: bash

  pcap_diff.py -i client.dump -i server.dump -o diff.pcap -f m

Ignore all IP Ids, TCP sequence and acknowledgement number

.. code-block:: bash

  pcap_diff.py -i client.dump -i server.dump -o diff.pcap -f ii -f sa

Do a diff over all packet headers including timestamps, ttl and checksums

.. code-block:: bash

  pcap_diff.py -i client.dump -i server.dump -o diff.pcap -c


License
=======

Copyright 2013 ETH Zurich, ISGINF, Bastian Ballmann
E-Mail: bastian.ballmann@inf.ethz.ch
Web: http://www.isg.inf.ethz.ch

This is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

It is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License.
If not, see <http://www.gnu.org/licenses/>.
