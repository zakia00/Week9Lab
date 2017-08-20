# Week9LabandAssignment
# Cybersecurity Week9Lab and Assignment - Zakia 

Time spent: 5 hours spent in total 

## User Stories

The following **required** functionality is completed:

Lab:
1. [x]  Required: Milestone 0: Networking Toolbox
2. [x]  Required: Milestone 1: Security-Flavored Net Tools
3. [x]  Required: Milestone 2: Grabbing Packets with tcpdump
4. [x]  Required: Milestone 3: Hello, Wireshark
5. [x]  Required: Milestone 4: Traffic Analysis — Mike's Computer is Acting Weird
6. [x]  Required: Milestone 5: Traffic Analysis — Mystery Meat Malware
7. [x]  Required: Milestone 6: Wi-Fi Hacking — Crack a Handshake
8. [x]  Required: Milestone 7: Wi-Fi Hacking — Grab a Handshake

The answers are written in wk9-lab.docx file.
The following advanced user stories are optional:

* [ ]  Bonus Milestone 8: Wi-Fi Hacking — Sniff Thy Neighbor's Packets

Assignment:
1. Overall approach, resources/tools used, findings: I used the Modern Honey Network honeypot for the assignment. I followed all the steps described in codepath course module. I started from cloning the MHN source and launching via Vagrant which created two VMS: honeypot and server. Then I opened shell on server and cloned mhn repo again inside the server vm and launched the pre-requisite install scripts: ./install_hpfeeds.sh ; ./install_mnemosyne.sh ; ./install_honeymap.sh. First I faced problem installing hpfeeds. Then I ran the command /opt/hpfeeds/env/bin/python -m pip install --upgrade pyopenssl to upgrade openssl which solved the problem. After that, I followed all the steps described in module. Finally, I accessed the MHN admin console via a browser at http://10.254.254.100 and login with the email / password I specified before. Now, in the browser, I could visit the Sensors page and listed mhn-honeypot-dionaea. I opened a Vagrant shell into the server VM and installed nmap via apt. Then I executed a scan against the honeypot VM using nmap.

I got total 1341 attacks as captured by nmap. The attacks used different protocols including smbd, epmapper, mssqld, pcap. The ports used for attacks are also presented in the attack list. Honeypot detected the date and time of the attacks along with the source ip address. All the detailed captures are shown in the attached figure.

## License

    Copyright [2017] [Kazi Zakia Sultana]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
