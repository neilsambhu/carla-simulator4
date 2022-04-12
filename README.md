# carla-simulator4
4/12/2022 3:19:54 PM: reinstall CARLA using Debian; handoff from https://github.com/neilsambhu/carla-simulator3 ; following https://carla.readthedocs.io/en/0.9.13/start_quickstart/

4/12/2022 3:29:13 PM: 
```
conda create -n carla-test python=3.7
```
4/12/2022 3:30:44 PM:
```
pip3 install --upgrade pip
```
```
pip3 install pygame numpy
```
4/12/2022 3:32:26 PM:
```
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 1AF1527DE64CB8D9
```
4/12/2022 3:33:09 PM:
```
sudo add-apt-repository "deb [arch=amd64] http://dist.carla.org/carla $(lsb_release -sc) main"
```
4/12/2022 3:34:03 PM:
```
(carla-test) nsambhu@SAMBHU19:/data/data1/GitHub/carla-simulator4$ sudo add-apt-repository "deb [arch=amd64] http://dist.carla.org/carla $(lsb_release -sc) main"

Repository: 'deb [arch=amd64] http://dist.carla.org/carla impish main'
Description:
Archive for codename: impish components: main
More info: http://dist.carla.org/carla
Adding repository.
Press [ENTER] to continue or Ctrl-c to cancel.Found existing deb entry in /etc/apt/sources.list.d/archive_uri-http_dist_carla_org_carla-impish.list
Adding deb entry to /etc/apt/sources.list.d/archive_uri-http_dist_carla_org_carla-impish.list
Found existing deb-src entry in /etc/apt/sources.list.d/archive_uri-http_dist_carla_org_carla-impish.list
Adding disabled deb-src entry to /etc/apt/sources.list.d/archive_uri-http_dist_carla_org_carla-impish.list
Ign:1 http://dist.carla.org/carla impish InRelease
Err:2 http://dist.carla.org/carla impish Release                                                                         
  404  Not Found [IP: 34.227.255.250 80]
Hit:3 http://us.archive.ubuntu.com/ubuntu impish InRelease                                                               
Get:4 https://dl.google.com/linux/chrome/deb stable InRelease [1,811 B]                                                  
Get:5 http://us.archive.ubuntu.com/ubuntu impish-security InRelease [110 kB]                                             
Hit:6 http://apt.pop-os.org/proprietary impish InRelease                                                                 
Hit:7 https://download.sublimetext.com apt/stable/ InRelease                                                             
Hit:8 https://linux.teamviewer.com/deb stable InRelease                                                                  
Get:9 https://dl.google.com/linux/chrome/deb stable/main amd64 Packages [1,089 B]                                        
Hit:10 http://apt.pop-os.org/release impish InRelease                                                                    
Get:11 http://us.archive.ubuntu.com/ubuntu impish-updates InRelease [115 kB]                
Get:12 http://us.archive.ubuntu.com/ubuntu impish-backports InRelease [101 kB]
Get:14 http://us.archive.ubuntu.com/ubuntu impish-security/universe Sources [23.6 kB]
Get:15 http://us.archive.ubuntu.com/ubuntu impish-security/main Sources [67.3 kB]              
Get:16 http://us.archive.ubuntu.com/ubuntu impish-security/main i386 Packages [127 kB]
Get:17 http://us.archive.ubuntu.com/ubuntu impish-security/main amd64 Packages [295 kB]
Get:18 http://us.archive.ubuntu.com/ubuntu impish-security/main Translation-en [72.1 kB]
Get:19 http://us.archive.ubuntu.com/ubuntu impish-security/main amd64 DEP-11 Metadata [20.2 kB]
Get:20 http://us.archive.ubuntu.com/ubuntu impish-security/main amd64 c-n-f Metadata [4,128 B]
Get:21 http://us.archive.ubuntu.com/ubuntu impish-security/universe i386 Packages [94.9 kB]
Get:22 http://us.archive.ubuntu.com/ubuntu impish-security/universe amd64 Packages [146 kB]
Get:23 http://us.archive.ubuntu.com/ubuntu impish-security/universe Translation-en [43.3 kB]
Get:24 http://us.archive.ubuntu.com/ubuntu impish-security/universe amd64 DEP-11 Metadata [3,616 B]
Get:25 http://us.archive.ubuntu.com/ubuntu impish-security/universe amd64 c-n-f Metadata [4,400 B]
Get:26 http://us.archive.ubuntu.com/ubuntu impish-updates/main Sources [102 kB]                
Get:27 http://us.archive.ubuntu.com/ubuntu impish-updates/main i386 Packages [167 kB]   
Get:28 http://us.archive.ubuntu.com/ubuntu impish-updates/main amd64 Packages [361 kB]
Get:29 http://us.archive.ubuntu.com/ubuntu impish-updates/main Translation-en [91.5 kB] 
Get:30 http://us.archive.ubuntu.com/ubuntu impish-updates/main amd64 DEP-11 Metadata [25.8 kB]
Get:31 http://us.archive.ubuntu.com/ubuntu impish-updates/universe amd64 Packages [186 kB]
Get:32 http://us.archive.ubuntu.com/ubuntu impish-updates/universe Translation-en [56.7 kB]
Get:33 http://us.archive.ubuntu.com/ubuntu impish-updates/universe amd64 DEP-11 Metadata [35.6 kB]
Get:34 http://us.archive.ubuntu.com/ubuntu impish-updates/multiverse amd64 DEP-11 Metadata [940 B]
Get:35 http://us.archive.ubuntu.com/ubuntu impish-backports/universe amd64 DEP-11 Metadata [16.4 kB]
Hit:13 https://packagecloud.io/slacktechnologies/slack/debian jessie InRelease            
Reading package lists... Done
E: The repository 'http://dist.carla.org/carla impish Release' does not have a Release file.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.
```
4/12/2022 3:34:49 PM: sudo add-apt-repository "deb [arch=amd64] http://dist.carla.org/carla bionic main"

4/12/2022 3:36:51 PM: maybe Pop!\_OS version is an issue.

4/12/2022 3:38:47 PM:
```
(carla-test) nsambhu@SAMBHU19:/data/data1/GitHub/carla-simulator4$ sudo add-apt-repository "deb [arch=amd64] http://dist.carla.org/carla bionic main"
Repository: 'deb [arch=amd64] http://dist.carla.org/carla bionic main'
Description:
Archive for codename: bionic components: main
More info: http://dist.carla.org/carla
Adding repository.
Press [ENTER] to continue or Ctrl-c to cancel.
Adding deb entry to /etc/apt/sources.list.d/archive_uri-http_dist_carla_org_carla-impish.list
Adding disabled deb-src entry to /etc/apt/sources.list.d/archive_uri-http_dist_carla_org_carla-impish.list
Hit:1 http://us.archive.ubuntu.com/ubuntu impish InRelease
Ign:2 http://dist.carla.org/carla impish InRelease                                                                       
Get:3 http://us.archive.ubuntu.com/ubuntu impish-security InRelease [110 kB]                                             
Get:4 http://dist.carla.org/carla bionic InRelease [2,338 B]                                                             
Hit:5 https://linux.teamviewer.com/deb stable InRelease                                                                  
Hit:6 https://dl.google.com/linux/chrome/deb stable InRelease                                                            
Hit:7 https://download.sublimetext.com apt/stable/ InRelease                                                             
Err:8 http://dist.carla.org/carla impish Release                                                                         
  404  Not Found [IP: 34.227.255.250 80]
Hit:9 http://apt.pop-os.org/proprietary impish InRelease                                                                 
Get:10 http://dist.carla.org/carla bionic/main amd64 Packages [2,124 B]                                                  
Get:11 http://us.archive.ubuntu.com/ubuntu impish-updates InRelease [115 kB]                                             
Hit:12 http://apt.pop-os.org/release impish InRelease                                                   
Get:13 http://us.archive.ubuntu.com/ubuntu impish-backports InRelease [101 kB]
Get:15 http://us.archive.ubuntu.com/ubuntu impish-updates/universe Sources [40.0 kB]
Get:16 http://us.archive.ubuntu.com/ubuntu impish-updates/main amd64 c-n-f Metadata [5,936 B]  
Get:17 http://us.archive.ubuntu.com/ubuntu impish-updates/universe i386 Packages [117 kB]
Get:18 http://us.archive.ubuntu.com/ubuntu impish-updates/universe amd64 Packages [188 kB]
Get:19 http://us.archive.ubuntu.com/ubuntu impish-updates/universe Translation-en [58.0 kB]
Get:20 http://us.archive.ubuntu.com/ubuntu impish-updates/universe amd64 c-n-f Metadata [5,384 B]
Hit:14 https://packagecloud.io/slacktechnologies/slack/debian jessie InRelease           
Reading package lists... Done
E: The repository 'http://dist.carla.org/carla impish Release' does not have a Release file.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.
```
4/12/2022 4:47:41 PM:
```
(base) nsambhu@SAMBHU19:/opt/carla-simulator/Import$ wget https://carla-releases.s3.eu-west-3.amazonaws.com/Linux/CARLA_0.9.13.tar.gz; wget https://carla-releases.s3.eu-west-3.amazonaws.com/Linux/CARLA_0.9.13_RSS.tar.gz
--2022-04-12 15:17:01--  https://carla-releases.s3.eu-west-3.amazonaws.com/Linux/CARLA_0.9.13.tar.gz
Resolving carla-releases.s3.eu-west-3.amazonaws.com (carla-releases.s3.eu-west-3.amazonaws.com)... 52.95.155.0
Connecting to carla-releases.s3.eu-west-3.amazonaws.com (carla-releases.s3.eu-west-3.amazonaws.com)|52.95.155.0|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 6680164671 (6.2G) [application/x-tar]
Saving to: ‘CARLA_0.9.13.tar.gz’

CARLA_0.9.13.tar.gz 100%[===================>]   6.22G  4.00MB/s    in 22m 9s  

2022-04-12 15:39:10 (4.80 MB/s) - ‘CARLA_0.9.13.tar.gz’ saved [6680164671/6680164671]

--2022-04-12 15:39:10--  https://carla-releases.s3.eu-west-3.amazonaws.com/Linux/CARLA_0.9.13_RSS.tar.gz
Resolving carla-releases.s3.eu-west-3.amazonaws.com (carla-releases.s3.eu-west-3.amazonaws.com)... 52.95.156.64
Connecting to carla-releases.s3.eu-west-3.amazonaws.com (carla-releases.s3.eu-west-3.amazonaws.com)|52.95.156.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 6853340526 (6.4G) [application/x-tar]
Saving to: ‘CARLA_0.9.13_RSS.tar.gz’

CARLA_0.9.13_RSS.ta 100%[===================>]   6.38G  4.99MB/s    in 18m 58s 

2022-04-12 15:58:09 (5.74 MB/s) - ‘CARLA_0.9.13_RSS.tar.gz’ saved [6853340526/6853340526]

```
4/12/2022 5:21:55 PM: https://carla.readthedocs.io/en/latest/adv_rendering_options/
```
DISPLAY=:0.GPU ./CarlaUE4.sh -vulkan
```
4/12/2022 6:25:19 PM:
```
python scenario_runner.py --scenario FollowLeadingVehicle_1 --record recording_files --reloadWorld
```