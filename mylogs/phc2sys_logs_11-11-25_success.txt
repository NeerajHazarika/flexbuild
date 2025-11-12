root@ls1028ardb:/home/debian# phc2sys -s eno0 -c CLOCK_REALTIME --step_threshold=1
time offset must be specified using -w or -O

usage: phc2sys [options]


 automatic configuration:
 -a             turn on autoconfiguration
 -r             synchronize system (realtime) clock
                repeat -r to consider it also as a time source
 manual configuration:
 -c [dev|name]  slave clock (CLOCK_REALTIME)
 -d [dev]       master PPS device
 -s [dev|name]  master clock
 -O [offset]    slave-master time offset (0)
 -w             wait for ptp4l
 common options:
 -f [file]      configuration file
 -E [pi|linreg] clock servo (pi)
 -P [kp]        proportional constant (0.7)
 -I [ki]        integration constant (0.3)
 -S [step]      step threshold (disabled)
 -F [step]      step threshold only on start (0.00002)
 -R [rate]      slave clock update rate in HZ (1.0)
 -N [num]       number of master clock readings per update (5)
 -L [limit]     sanity frequency limit in ppb (200000000)
 -M [num]       NTP SHM segment number (0)
 -u [num]       number of clock updates in summary stats (0)
 -n [num]       domain number (0)
 -x             apply leap seconds by servo instead of kernel
 -z [path]      server address for UDS (/var/run/ptp4l)
 -l [num]       set the logging level to 'num' (6)
 -t [tag]       add tag to log messages
 -m             print messages to stdout
 -q             do not print messages to the syslog
 -v             prints the software version and exits
 -h             prints this message and exits

root@ls1028ardb:/home/debian# phc2sys -s eno0 -c CLOCK_REALTIME -w -m -F 1.0
phc2sys[1205.247]: CLOCK_REALTIME phc offset 1762884964848853638 s0 freq +100000000 delay    684
phc2sys[1206.247]: CLOCK_REALTIME phc offset 1762884964737708471 s1 freq   -2226 delay    612
phc2sys[1207.248]: CLOCK_REALTIME phc offset 1762884967459282841 s2 freq +100000000 delay    680
phc2sys[1208.250]: CLOCK_REALTIME phc offset 1762884967347860299 s2 freq +100000000 delay    612
phc2sys[1209.251]: CLOCK_REALTIME phc offset 1762884967236725473 s2 freq +100000000 delay    612
phc2sys[1210.251]: CLOCK_REALTIME phc offset 1762884967125591585 s2 freq +100000000 delay    612
phc2sys[1211.251]: CLOCK_REALTIME phc offset 1762884967014461577 s2 freq +100000000 delay    612
phc2sys[1212.251]: CLOCK_REALTIME phc offset 1762884966903332511 s2 freq +100000000 delay    684
phc2sys[1213.251]: CLOCK_REALTIME phc offset 1762884966792201696 s2 freq +100000000 delay    684
phc2sys[1214.251]: CLOCK_REALTIME phc offset 1762884966681059913 s2 freq +100000000 delay    648
phc2sys[1215.252]: CLOCK_REALTIME phc offset 1762884966569915775 s2 freq +100000000 delay    900
phc2sys[1216.252]: CLOCK_REALTIME phc offset 1762884966458783562 s2 freq +100000000 delay    612
phc2sys[1217.252]: CLOCK_REALTIME phc offset 1762884966347650148 s2 freq +100000000 delay    612
phc2sys[1218.252]: CLOCK_REALTIME phc offset 1762884966236518584 s2 freq +100000000 delay    720
phc2sys[1219.252]: CLOCK_REALTIME phc offset 1762884966125385824 s2 freq +100000000 delay    684
phc2sys[1220.253]: CLOCK_REALTIME phc offset 1762884966014253159 s2 freq +100000000 delay    612
phc2sys[1221.253]: CLOCK_REALTIME phc offset 1762884965903120683 s2 freq +100000000 delay    684
phc2sys[1222.253]: CLOCK_REALTIME phc offset 1762884965791987126 s2 freq +100000000 delay    900
phc2sys[1223.253]: CLOCK_REALTIME phc offset 1762884965680850837 s2 freq +100000000 delay    612
phc2sys[1224.253]: CLOCK_REALTIME phc offset 1762884965569719645 s2 freq +100000000 delay    612
phc2sys[1225.253]: CLOCK_REALTIME phc offset 1762884965458587763 s2 freq +100000000 delay    612
phc2sys[1226.256]: CLOCK_REALTIME phc offset 1762884965347240045 s2 freq +100000000 delay    648
phc2sys[1227.257]: CLOCK_REALTIME phc offset 1762884965235984006 s2 freq +100000000 delay    648
phc2sys[1228.258]: CLOCK_REALTIME phc offset 1762884965124716420 s2 freq +100000000 delay    648
phc2sys[1229.260]: CLOCK_REALTIME phc offset 1762884965013420382 s2 freq +100000000 delay    648
phc2sys[1230.260]: CLOCK_REALTIME phc offset 1762884964902245419 s2 freq +100000000 delay    720
phc2sys[1231.261]: CLOCK_REALTIME phc offset 1762884964791062429 s2 freq +100000000 delay    684
phc2sys[1232.261]: CLOCK_REALTIME phc offset 1762884964679927237 s2 freq +100000000 delay    648
phc2sys[1233.262]: CLOCK_REALTIME phc offset 1762884964568724433 s2 freq +100000000 delay    720
phc2sys[1234.262]: CLOCK_REALTIME phc offset 1762884964457591663 s2 freq +100000000 delay    612
phc2sys[1235.262]: CLOCK_REALTIME phc offset 1762884964346460545 s2 freq +100000000 delay    936
phc2sys[1236.263]: CLOCK_REALTIME phc offset 1762884964235324894 s2 freq +100000000 delay    612
phc2sys[1237.263]: CLOCK_REALTIME phc offset 1762884964124186163 s2 freq +100000000 delay    612
phc2sys[1238.263]: CLOCK_REALTIME phc offset 1762884964013011524 s2 freq +100000000 delay    612
phc2sys[1239.265]: clockcheck: clock jumped forward or running faster than expected!
phc2sys[1239.268]: CLOCK_REALTIME phc offset 1762884967346596950 s0 freq +100000000 delay    612
phc2sys[1240.272]: CLOCK_REALTIME phc offset 1762884967234672551 s2 freq -100000000 delay    648
phc2sys[1241.272]: CLOCK_REALTIME phc offset 1762884967325595845 s2 freq +100000000 delay    748
phc2sys[1242.272]: CLOCK_REALTIME phc offset 1762884967214469213 s2 freq +100000000 delay    684
phc2sys[1243.272]: CLOCK_REALTIME phc offset 1762884967103336732 s2 freq +100000000 delay    612
phc2sys[1244.273]: CLOCK_REALTIME phc offset 1762884966992205054 s2 freq +100000000 delay    648
phc2sys[1245.273]: CLOCK_REALTIME phc offset 1762884966881070133 s2 freq +100000000 delay    612
phc2sys[1246.275]: CLOCK_REALTIME phc offset 1762884966769755104 s2 freq +100000000 delay    612
phc2sys[1247.275]: CLOCK_REALTIME phc offset 1762884966658607382 s2 freq +100000000 delay    612
phc2sys[1248.276]: CLOCK_REALTIME phc offset 1762884966547410010 s2 freq +100000000 delay    648
phc2sys[1249.276]: CLOCK_REALTIME phc offset 1762884966436278580 s2 freq +100000000 delay    648
phc2sys[1250.277]: CLOCK_REALTIME phc offset 1762884966325007371 s2 freq +100000000 delay    612
phc2sys[1251.278]: CLOCK_REALTIME phc offset 1762884966213791398 s2 freq +100000000 delay    612
phc2sys[1252.278]: CLOCK_REALTIME phc offset 1762884966102661696 s2 freq +100000000 delay    612
^Cphc2sys[1252.889]: CLOCK_REALTIME phc offset 1762884966034848773 s2 freq +100000000 delay    648
root@ls1028ardb:/home/debian# systemctl status systemd-timesyncd
● systemd-timesyncd.service - Network Time Synchronization
     Loaded: loaded (/lib/systemd/system/systemd-timesyncd.servic>
     Active: active (running) since Tue 2025-11-11 18:13:57 UTC; >
       Docs: man:systemd-timesyncd.service(8)
   Main PID: 192 (systemd-timesyn)
     Status: "Contacted time server 148.251.54.81:123 (2.debian.p>
      Tasks: 2 (limit: 3836)
     Memory: 1.3M
        CPU: 152ms
     CGroup: /system.slice/systemd-timesyncd.service
             └─192 /lib/systemd/systemd-timesyncd

Jun 26 14:58:42 ls1028ardb systemd[1]: Starting systemd-timesyncd>
Jun 26 14:58:43 ls1028ardb systemd-timesyncd[192]: System clock t>
Nov 11 18:13:57 ls1028ardb systemd[1]: Started systemd-timesyncd.>
Nov 11 18:16:11 ls1028ardb systemd-timesyncd[192]: Contacted time>
Nov 11 18:16:11 ls1028ardb systemd-timesyncd[192]: Initial clock >
root@ls1028ardb:/home/debian# systemctl stop systemd-timesyncd
root@ls1028ardb:/home/debian# systemctl disable systemd-timesyncd
Removed "/etc/systemd/system/dbus-org.freedesktop.timesync1.service".
Removed "/etc/systemd/system/sysinit.target.wants/systemd-timesyncd.service".
root@ls1028ardb:/home/debian# phc2sys -s eno0 -c CLOCK_REALTIME -w -m -F 1.0
phc2sys[1326.319]: CLOCK_REALTIME phc offset 1762884961257625290 s0 freq +100000000 delay    612
phc2sys[1327.319]: CLOCK_REALTIME phc offset 1762884961146473269 s1 freq   -2213 delay    612
phc2sys[1328.319]: CLOCK_REALTIME phc offset     -4688 s2 freq   -6901 delay    680
phc2sys[1329.319]: CLOCK_REALTIME phc offset       199 s2 freq   -3421 delay    680
phc2sys[1330.320]: CLOCK_REALTIME phc offset      1625 s2 freq   -1935 delay    680
phc2sys[1331.320]: CLOCK_REALTIME phc offset      1561 s2 freq   -1511 delay    680
phc2sys[1332.320]: CLOCK_REALTIME phc offset      1077 s2 freq   -1527 delay    680
^Cphc2sys[1333.257]: CLOCK_REALTIME phc offset       620 s2 freq   -1661 delay    720
root@ls1028ardb:/home/debian# phc2sys -s eno0 -c CLOCK_REALTIME -w -m -F 1.0
phc2sys[1341.427]: CLOCK_REALTIME phc offset     -2133 s0 freq   -1661 delay    800
phc2sys[1342.429]: CLOCK_REALTIME phc offset     -2462 s2 freq   -1989 delay    760
phc2sys[1343.430]: CLOCK_REALTIME phc offset     -2492 s2 freq   -4481 delay    680
phc2sys[1344.431]: CLOCK_REALTIME phc offset         2 s2 freq   -2735 delay    680
phc2sys[1345.432]: CLOCK_REALTIME phc offset       733 s2 freq   -2003 delay    680
phc2sys[1346.432]: CLOCK_REALTIME phc offset       751 s2 freq   -1765 delay    760
phc2sys[1347.433]: CLOCK_REALTIME phc offset       507 s2 freq   -1784 delay    800
phc2sys[1348.433]: CLOCK_REALTIME phc offset       296 s2 freq   -1843 delay    680
phc2sys[1349.437]: CLOCK_REALTIME phc offset       119 s2 freq   -1931 delay    720
phc2sys[1350.438]: CLOCK_REALTIME phc offset        60 s2 freq   -1955 delay    680
phc2sys[1351.441]: CLOCK_REALTIME phc offset        15 s2 freq   -1982 delay    680
phc2sys[1352.443]: CLOCK_REALTIME phc offset       -13 s2 freq   -2005 delay    720
phc2sys[1353.444]: CLOCK_REALTIME phc offset        12 s2 freq   -1984 delay    720
phc2sys[1354.444]: CLOCK_REALTIME phc offset       -19 s2 freq   -2011 delay    720
phc2sys[1355.444]: CLOCK_REALTIME phc offset        18 s2 freq   -1980 delay    760
phc2sys[1356.445]: CLOCK_REALTIME phc offset       -12 s2 freq   -2005 delay    680
phc2sys[1357.447]: CLOCK_REALTIME phc offset        -7 s2 freq   -2003 delay    680
phc2sys[1358.447]: CLOCK_REALTIME phc offset        -3 s2 freq   -2001 delay    760
phc2sys[1359.448]: CLOCK_REALTIME phc offset        -7 s2 freq   -2006 delay    680
phc2sys[1360.448]: CLOCK_REALTIME phc offset        15 s2 freq   -1986 delay    760
phc2sys[1361.448]: CLOCK_REALTIME phc offset       -19 s2 freq   -2016 delay    720
phc2sys[1362.450]: CLOCK_REALTIME phc offset        -8 s2 freq   -2011 delay    680
phc2sys[1363.450]: CLOCK_REALTIME phc offset        28 s2 freq   -1977 delay    800
phc2sys[1364.450]: CLOCK_REALTIME phc offset       -35 s2 freq   -2032 delay    720
phc2sys[1365.451]: CLOCK_REALTIME phc offset        27 s2 freq   -1980 delay    680
phc2sys[1366.451]: CLOCK_REALTIME phc offset        18 s2 freq   -1981 delay    760
phc2sys[1367.451]: CLOCK_REALTIME phc offset       -16 s2 freq   -2010 delay    680
phc2sys[1368.451]: CLOCK_REALTIME phc offset        -1 s2 freq   -1999 delay    680
phc2sys[1369.452]: CLOCK_REALTIME phc offset        -2 s2 freq   -2001 delay    680
phc2sys[1370.452]: CLOCK_REALTIME phc offset       -11 s2 freq   -2010 delay    720
phc2sys[1371.452]: CLOCK_REALTIME phc offset        30 s2 freq   -1973 delay   1200
phc2sys[1372.453]: CLOCK_REALTIME phc offset       -18 s2 freq   -2012 delay    680
phc2sys[1373.453]: CLOCK_REALTIME phc offset       -21 s2 freq   -2020 delay    720
phc2sys[1374.453]: CLOCK_REALTIME phc offset        14 s2 freq   -1991 delay    800
phc2sys[1375.453]: CLOCK_REALTIME phc offset       -19 s2 freq   -2020 delay    720
phc2sys[1376.454]: CLOCK_REALTIME phc offset        21 s2 freq   -1986 delay    680
phc2sys[1377.455]: CLOCK_REALTIME phc offset        12 s2 freq   -1988 delay    680
phc2sys[1378.456]: CLOCK_REALTIME phc offset       -24 s2 freq   -2021 delay    800
phc2sys[1379.456]: CLOCK_REALTIME phc offset        12 s2 freq   -1992 delay    680
phc2sys[1380.456]: CLOCK_REALTIME phc offset        -1 s2 freq   -2001 delay    680
phc2sys[1381.456]: CLOCK_REALTIME phc offset        -4 s2 freq   -2005 delay    800
phc2sys[1382.457]: CLOCK_REALTIME phc offset        16 s2 freq   -1986 delay    680
phc2sys[1383.458]: CLOCK_REALTIME phc offset         7 s2 freq   -1990 delay    680
phc2sys[1384.459]: CLOCK_REALTIME phc offset        -2 s2 freq   -1997 delay    760
^Cphc2sys[1384.752]: CLOCK_REALTIME phc offset        -8 s2 freq   -2004 delay    680
root@ls1028ardb:/home/debian# 