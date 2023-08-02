1) Download iso file from vidoo iso from the link :
   https://nurdllc-my.sharepoint.com/:u:/g/personal/mirzam_comodo_net/EbBZlBjYBfFBrftjoW7Ei-wBVkE1msyutcnaRT_8MTlz1w?e=2XEQI4
   
3) Create a bootable usb using the ISO file from no 1 [ check google how to burn iso files to usb for ubuntu]
4) Boot from usb and either install on hardisk or Try without install option from the boot menu
5) Once installed / logged in ; go to terminal and run following comand to install

      docker run --net host -v /var/run/docker.sock:/var/run/docker.sock --restart=always --name orchestrator-vhubzz us-east4-docker.pkg.dev/softhub-354014/softhub/orchestrator:latest /root/orchestrator vhub -start -option provision -username=your-Ezlo-username -password=your-ezlo-password -zwave=/dev/ttyUSB1 -vidoo

   Notes: 
       Change <your-Ezlo-username> and <your-ezlo-password> fields with the credentials you have on the MiOS platform.
       CCTV + AI support enabled with version 0.7.3
       To include CCTV + AI, the “-vidoo” parameter is required.
       To enable Z-Wave support (via USB Z-Wave Stick), use this parameter: -zwave=/dev/ttyUSB1
       If you do not have a USB stick, remove the parameter.

5) Go to localhost on your browser to login to vidoo app

