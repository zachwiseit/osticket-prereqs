<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial covers the requirements and installation process for the open-source help desk ticketing system, osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- Windows App

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)
- macOS Sonama 14.6.1

<h2>List of Prerequisites</h2>

- Azure Virtual Machines
- ISS
- Install 
- Item 4
- Item 5

<h2>Installation Steps</h2>

<p>
1. First step of course is to log into Azure and create your virtual machines. 
   You will need to create a "Virtual machine name" and choose a "Region". 

<img width="1440" alt="OST_1" src="https://github.com/user-attachments/assets/83241932-5a8c-480f-bd2c-1764de12eb34" />

2 Scroll down to "image" and choose Windows 10 Pro. 
  Then for "Size" choose whichever option you like as long as the option has at least 2 vcpus. 
  
![image](https://github.com/user-attachments/assets/b9026065-2a61-406e-a5cb-b90806dc3da5)

3 At the bottom of the page create a "Username", "Password", and confirm licensing before you click "Next: Disks>". 

![image](https://github.com/user-attachments/assets/e33d2e70-8e1b-454f-9bee-0deb33235e06)

4 Click "Next: Networking>"

![image](https://github.com/user-attachments/assets/afd1d0d8-8811-4c52-9219-c3cbd3e58166)

5 Click "Reveiw + create" 

![image](https://github.com/user-attachments/assets/41b10f99-876c-4449-8091-b5c31c249ff1)

6 Here you will see the final costs for your VM. At the bottom click "Create". 

![image](https://github.com/user-attachments/assets/6599a392-28ef-4e8c-9e73-9d9d8f2a6868)

7 Now Azure will begin to build your your Virtual Machine and the necessary assets. 

![image](https://github.com/user-attachments/assets/2edcba34-2c58-40cd-873d-5685b1a3edee)

8 Now that the deployment is complete go back to the Home page and click on "Virtual Machines".

![image](https://github.com/user-attachments/assets/d132af97-44db-4bb5-8f36-43c4928b4bc3)

9 Here you will need to copy your VM's "Public IP address". 

![image](https://github.com/user-attachments/assets/0da6cc6f-c9f0-48d8-a65c-9cb108889641)

10 Next start up the Windows App and click Add PC

<img width="1440" alt="OST_11" src="https://github.com/user-attachments/assets/5d9467a9-7e49-4d72-b747-814d75887baa" />

11 PC name: Public IP address 
   Friendly name: Your choice
   Click add 

<img width="1440" alt="OST_12" src="https://github.com/user-attachments/assets/4c9038bc-b263-40d1-a06c-87b03cfb1332" />

12 Put in the username and password you created and click continue 

<img width="1440" alt="OST_17" src="https://github.com/user-attachments/assets/24acb3fa-57cb-468d-9b91-3c23816aeca6" />

13 Confirm you're connecting to the correct address and click continue. 

<img width="1440" alt="OST_18" src="https://github.com/user-attachments/assets/cc4868d4-a4fe-4143-9cdb-73be2d5bfef0" />

14 Click no for everything (These settings don’t matter) and then continue. 

<img width="1440" alt="OST_19" src="https://github.com/user-attachments/assets/dd7e08ec-0ba5-4347-b010-5459ca76949c" />

15 Now that your are at the desktop open up Microsoft Edge. 

<img width="1440" alt="OST_20" src="https://github.com/user-attachments/assets/7a1efa65-f03f-4c0e-9f00-a7fe81da9f22" />

16 Copy this link https://drive.usercontent.google.com/download?id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD&export=download&authuser=0 and Download osTicket-Installation.

<img width="1440" alt="OST_22" src="https://github.com/user-attachments/assets/5f958162-6143-41f8-9143-cb9709bc2ad2" />

18 At the top Right click Downloads and Open downloads folder. 

<img width="1440" alt="OST_24" src="https://github.com/user-attachments/assets/cdba79f1-0d88-4bbf-ae88-964666c2e7e9" />

19 Move the zipp file to the Desktop. 

<img width="1440" alt="OST_25" src="https://github.com/user-attachments/assets/e7018d98-d06b-464c-a738-aa01c0f1b1df" />

20 Right click the zipped file and Extract all

<img width="1440" alt="OST_26" src="https://github.com/user-attachments/assets/092c5d48-d096-406d-92b7-ded06b9270da" />

21 Now select your preferred extraction destination and click extract. 

<img width="1440" alt="OST_27" src="https://github.com/user-attachments/assets/baa8f711-746c-4604-9208-40ad5375ca98" />

22 Now that the folder is extracted you need to install/enable IIS(Internet Information Services) in Windows with CGI(Common Gateway Interface) 

<img width="1440" alt="OST_28" src="https://github.com/user-attachments/assets/a6fcb3be-348d-47bb-b139-f091db1ef2f1" />

23 To do this first open up the Control panel from the search bar. 

<img width="1440" alt="OST_29" src="https://github.com/user-attachments/assets/108e4eb3-8bd1-4b43-b9a3-55b30581e1a8" />

24 Click on Programs.

<img width="1440" alt="OST_31" src="https://github.com/user-attachments/assets/3ca052c2-69f6-4090-9b2d-07caf2639e5a" />

25 On the left click "Turn Windows features on or off". 

<img width="1440" alt="OST_33" src="https://github.com/user-attachments/assets/4c28c064-9778-4e87-8bf0-ff45efe80ac4" />

26 Scroll down to "Internet Information Service", check the box next to it, and click the addition symbol next to it.

<img width="1440" alt="OST_34" src="https://github.com/user-attachments/assets/da0c8b54-2aba-4cde-8c85-d73e7087f7f7" />

27 From there expand "World Wide Web services".

<img width="1440" alt="OST_36" src="https://github.com/user-attachments/assets/f22ea474-4f6d-4e7a-a2bf-8e6777e84a5a" />

28 Expand "Application Development Features" as well.

<img width="1440" alt="OST_37" src="https://github.com/user-attachments/assets/cb6f5b87-36d4-4e9c-9d02-27ce8cb17a73" />

29 Now check the box next to CGI to enable Common Gateway Interface. 

<img width="1440" alt="OST_38" src="https://github.com/user-attachments/assets/2f787854-6160-4e9e-90a1-d38e2fa71ee4" />

30 Click Ok and it will begin to install the web server and when it is done click close.  

<img width="1440" alt="OST_40" src="https://github.com/user-attachments/assets/9008feac-92a2-4155-8069-a3ad6077ed3b" />

32 Now if you enter 127.0.0.1 into the search bar this web page will load to show that CGI and IIS are active. 

<img width="1440" alt="OST_42" src="https://github.com/user-attachments/assets/6645ff69-5437-42dc-8eb2-0115ffab862f" />

33 Next you need to install PHP manager for IIS from the Osticket-Installation-Files folder.

<img width="1440" alt="OST_43" src="https://github.com/user-attachments/assets/44ae048e-743e-458f-8488-82cae5e1cf16" />

34 Go into that folder and click PHPManagerForIIS_V1.5.0

<img width="1440" alt="OST_44" src="https://github.com/user-attachments/assets/9bc0eb4b-2ca2-41bc-9137-de3d5558ae71" />

35 click next 

<img width="1440" alt="OST_45" src="https://github.com/user-attachments/assets/2ce308c3-f3ce-4d98-9652-95922f30bf68" />

36  click I agree and Next 

<img width="1440" alt="OST_46" src="https://github.com/user-attachments/assets/a4c54807-7d32-40e0-b4a8-ea418b42904d" />

37 Click Yes to allow to make changes and after it is installed click close. 

<img width="1440" alt="OST_47" src="https://github.com/user-attachments/assets/39d80ea2-128a-40e0-84fe-516dc53c1e3a" />

38 From the same Folder install the Rewrite Module. 

<img width="1440" alt="OST_48" src="https://github.com/user-attachments/assets/ecdfb75e-8c15-418d-a814-1d58e668589b" />

39 After you click on the Rewrite Module click install 

<img width="1440" alt="OST_49" src="https://github.com/user-attachments/assets/fbe55284-d515-4639-9ec3-c787faf41833" />

40 After it is installed click finish. 

<img width="1440" alt="OST_51" src="https://github.com/user-attachments/assets/4e7ad52c-e0ec-45c7-8650-4a70fdeefc8d" />

41 Next you need to create a directory on the C drive named PHP.
   Right click on the windows Icon and and open FIle Explorer.

<img width="1440" alt="OST_52" src="https://github.com/user-attachments/assets/40118b83-dbb4-49d5-a574-caa026d63fa1" />

42 Open Windows (c:)and create a new folder.

<img width="1440" alt="OST_54" src="https://github.com/user-attachments/assets/ffc1cf64-a419-4f8d-8ce2-33a6406f5104" />

43 Name it PHP. 

<img width="1440" alt="OST_55" src="https://github.com/user-attachments/assets/b8932edd-f90c-48a4-9340-6ce0b1a0113b" />

44 Now from the "osTicket-Installation_Files" Folder unzip "php-7.3.8-nts-Win32-VC15-x86.zip".

<img width="1440" alt="OST_56" src="https://github.com/user-attachments/assets/d35cb158-61e5-46f2-ab04-4ad9ddd01971" />

45 Right click "php-7.3.8-nts-Win32-VC15-x86.zip" and Extract All.

<img width="1440" alt="OST_57" src="https://github.com/user-attachments/assets/acaee770-6515-46ab-ae7f-703bd5f8f0e2" />

46 Click Browse.

<img width="1440" alt="OST_58" src="https://github.com/user-attachments/assets/1a90f059-60a0-40b8-ba5f-065a437a51f5" />

47 Scroll down to Windows (C:) and select PHP.

<img width="1440" alt="OST_59" src="https://github.com/user-attachments/assets/8c89542e-2889-4914-bcbc-15e4a3235f50" />

48 Now click Select Folder.

<img width="1440" alt="OST_60" src="https://github.com/user-attachments/assets/a8bd362c-48a8-4086-b429-e7270e9dcc38" />

49 Click Extract and it will begin to unzip everything to the PHP folder. 

<img width="1440" alt="OST_61" src="https://github.com/user-attachments/assets/3fba78ec-842f-41c3-bcf6-441bbb5bea20" />

50 Now you can see everything in PHP that will be necessary for later.

<img width="1440" alt="OST_62" src="https://github.com/user-attachments/assets/d44d8b65-bb71-4f68-ac58-a6c8377409ff" />

51 Next you need to install VC_redist.x86 from the "osTicket-Installation-Files" folder.

<img width="1440" alt="OST_63" src="https://github.com/user-attachments/assets/235781a4-349c-432c-bf25-d0c63878f4c4" />

52 Click VC_redist.x86, agree to the license, and click install. 

<img width="1440" alt="OST_64" src="https://github.com/user-attachments/assets/deb1cdab-119d-4838-8133-d1b8a6f0e3f2" />

53 After installation is successful click close. 

<img width="1440" alt="OST_65" src="https://github.com/user-attachments/assets/99456c1c-1649-4247-ae20-052bf365302b" />

54 Next install mysql-5.5.62-win32 (The data base where all the data will be stored).

<img width="1440" alt="OST_66" src="https://github.com/user-attachments/assets/f9d61bab-b5b9-4aac-9847-e346c733204b" />

56 Click on mysql-5.5.62-win32 then click next. 

<img width="1440" alt="OST_67" src="https://github.com/user-attachments/assets/1c0bb468-5844-4aad-9e58-9a632d442b9b" />

57 Accept the terms and click Next.

<img width="1440" alt="OST_68" src="https://github.com/user-attachments/assets/d60df1e6-bebb-4499-b0f8-29358ac14150" />

58 Choose Typical Installation.

<img width="1440" alt="OST_69" src="https://github.com/user-attachments/assets/c41102f3-94cf-462b-8c8c-cb38debadf63" />

59 CLick Install.

<img width="1440" alt="OST_70" src="https://github.com/user-attachments/assets/520e9463-12fd-4135-8cd1-5bf54c075037" />

60 Check the Launch Confiiguration Wizard box and click Finish. 

<img width="1440" alt="OST_71" src="https://github.com/user-attachments/assets/3554a836-0cd2-4dbd-b853-6ec06e652a6e" />

61 CLick next 

<img width="1440" alt="OST_72" src="https://github.com/user-attachments/assets/25a0cac3-4be7-4cf1-ad1a-068d7327e115" />

62 Check Standard Configuration and click next 

<img width="1440" alt="OST_73" src="https://github.com/user-attachments/assets/ab372994-2943-43f3-bf27-e6e60f076f40" />

63 Click next 

<img width="1440" alt="OST_74" src="https://github.com/user-attachments/assets/e0978be9-ef50-4451-8d45-dcd6e03aa138" />

64 Type in a password thats simple for this scenario like "root". It is very important be sure to write it down. 

<img width="1440" alt="OST_75" src="https://github.com/user-attachments/assets/8ab15f36-e10c-4af6-8c6d-67ae4dc1d812" />

65 Click Execute 

<img width="1440" alt="OST_78" src="https://github.com/user-attachments/assets/c39b7374-676c-4b3a-a001-8003321bec9a" />

66 Click Finish and now the Database is ready to go. 

<img width="1440" alt="OST_80" src="https://github.com/user-attachments/assets/fd302fc7-1413-40ea-805f-b6bdf428f671" />

67 Now you need to open IIS up as an Admin. 
   In the Windows search bar and search for Internet Information Services(IIS)

<img width="1440" alt="OST_81" src="https://github.com/user-attachments/assets/1865ee21-96ef-4257-9657-e79e17d5f011" />

68 Right click and run as administrator

<img width="1440" alt="OST_83" src="https://github.com/user-attachments/assets/53397af3-6ae7-4f75-878e-760536499a1c" />

69 Now register PHP from within IIS. This will make the webserver aware of the existence of PHP on the computer.
   Open PHP Manager.

<img width="1440" alt="OST_84" src="https://github.com/user-attachments/assets/e44f09d2-47c3-4787-af41-d49eb04f5948" />

70 Click Register new PHP version 

<img width="1440" alt="OST_85" src="https://github.com/user-attachments/assets/a9630d5c-aea6-4bb5-bd3c-6342c6b2dda3" />

71 Click the three dotted button next to the search bar to browse for the file. 

<img width="1440" alt="OST_86" src="https://github.com/user-attachments/assets/8b6a1de5-ce4b-4fd4-8dc9-8a454a313d2e" />

72 Scroll down to Windows (c:) then click the PHP file created earlier. 

<img width="1440" alt="OST_87" src="https://github.com/user-attachments/assets/9d3dc196-8c53-444e-8cac-f8ed3cfe98c6" />

73 Click on th php-cgi executable. 

<img width="1440" alt="OST_88" src="https://github.com/user-attachments/assets/65c383f1-e236-4a5b-ad47-090322ea40ac" />

74 After clicking it if your screen looks like this you can press ok and continue. 

<img width="1440" alt="OST_89" src="https://github.com/user-attachments/assets/48c3a5f7-8774-48dc-acd1-a1faeb3878b9" />

76 Now reload IIS to the right under "Manage Server" 

<img width="1440" alt="OST_92" src="https://github.com/user-attachments/assets/ad4084a6-f65f-43b3-8c88-192fb8557bd8" />

77 Click Stop and then Start. This will Reload IIS. 

<img width="1440" alt="OST_93" src="https://github.com/user-attachments/assets/685d20e7-d830-42a5-bbd4-8057c79e7937" />

78 Next you need to install osTicket v1.15.8 from the Installation Files and copy the "upload"  folder into "c:\inetpub\wwwroot"
   Right click osTicket v1.15.8 and click extract all. 
   
<img width="1440" alt="OST_94" src="https://github.com/user-attachments/assets/25d7088f-27d5-4d2b-8bf8-2dee86cfff69" />

79 Click Extract

<img width="1440" alt="OST_95" src="https://github.com/user-attachments/assets/cca04f16-e4db-45dc-a917-bae976e2adf6" />

80 Wait for the file to copy. 

<img width="1440" alt="OST_96" src="https://github.com/user-attachments/assets/d9af155a-d559-4943-af98-1a1c4385eea2" />

81 Now that it is complete open up the osTicket v1.15.8.

<img width="1440" alt="OST_97" src="https://github.com/user-attachments/assets/c7dfd826-76c3-410c-9c89-8d91750b9c59" />

82 Open inetpub

<img width="1440" alt="OST_98" src="https://github.com/user-attachments/assets/02fed33e-6744-4025-839a-3e9cceb4f623" />

83 Open wwwroot

<img width="1440" alt="OST_99" src="https://github.com/user-attachments/assets/f4d9e2a5-30a4-4b38-9e04-f9b2e2b913da" />

84 Copy the upload file from osTicket-v1.15.8

<img width="1440" alt="OST_100" src="https://github.com/user-attachments/assets/4fbd26bd-02e0-44df-9a20-18d488332dea" />

85 Paste it into wwwroot

<img width="1440" alt="OST_102" src="https://github.com/user-attachments/assets/7c1c0ff8-cf4b-42a4-a285-fd455ffec5ab" />

87 Right click upload and rename the file to "osTicket".

<img width="1440" alt="OST_104" src="https://github.com/user-attachments/assets/afc4adc4-43aa-458d-8cbd-a810dfe1c9c5" />

88 Exactly like this DO NOT name it something else.

<img width="1440" alt="OST_105" src="https://github.com/user-attachments/assets/0a589b51-0e50-4c36-acf8-e5e3b50ed8d8" />

89 In osTicket-vm Home stop and start the server again. 

<img width="1440" alt="OST_106" src="https://github.com/user-attachments/assets/c9976918-7639-4011-b92e-6e94abdc3658" />

91 In IIS click the drop down arrow to the left of "Sites" then the arrow for "Default Web Site" and the "osTicket" file.

<img width="1440" alt="OST_108" src="https://github.com/user-attachments/assets/9d42f84a-5e40-4eb0-b373-b59800d9adab" />

92 On the right under Manage Folder click "Browse *:80".

<img width="1440" alt="OST_109" src="https://github.com/user-attachments/assets/9835ac3a-a148-4c91-8289-63252f0f56d4" />

93 Clicking that will load the OS Ticket site like this. Also some of the extensions are not enabled. Changing that is the next step. 

<img width="1440" alt="OST_110" src="https://github.com/user-attachments/assets/b49a91e2-aa29-42d1-8aea-f475172a61b3" />

94 Go back to IIS click sites, click Default and then osTicket.
   
<img width="1440" alt="OST_111" src="https://github.com/user-attachments/assets/17d8944b-3a47-4b5a-b6ab-9752d6513901" />

95 From there double-click PHP Manager.
   In PHP Manager click Enable or Disable an extension.

<img width="1440" alt="OST_112" src="https://github.com/user-attachments/assets/7f56ccc8-3ff4-44d6-bf89-f3ea66c85ffa" />

96 RIght click and enable these three extensions. 
   php_imap.dll
<img width="1440" alt="OST_113" src="https://github.com/user-attachments/assets/f10ed9ba-6db2-4a89-b0a8-8c1e46bef8de" />

97 php_intl.dll

<img width="1440" alt="OST_114" src="https://github.com/user-attachments/assets/0caaf462-f60d-4a85-a0ae-4e84a14cd0f4" />

98 php_opcache.dll

<img width="1440" alt="OST_115" src="https://github.com/user-attachments/assets/7fffb4ce-9e58-4d5b-9edc-de7fcecc1049" />

99 Now at the top you can see all the ones that are enabled.

<img width="1440" alt="OST_116" src="https://github.com/user-attachments/assets/baaf7981-e173-4ca7-8426-05569a6e5348" />

100 Back at the web page you wont see the changes until you refresh the web page.

<img width="1440" alt="OST_117" src="https://github.com/user-attachments/assets/f3e2fd3d-5b0b-4438-889a-97e051fc80a7" />

101 After the refresh you will see the changes and they should be enabled like this. 

<img width="1440" alt="OST_118" src="https://github.com/user-attachments/assets/59136578-1b5c-4d74-9f22-162e06c16457" />

103 Now you need to rename ost-config.php 
    Go into the osTicket file.
<img width="1440" alt="OST_120" src="https://github.com/user-attachments/assets/3950816a-8655-458d-8a20-4afa1403f20e" />

104 From there open "include"

<img width="1440" alt="OST_121" src="https://github.com/user-attachments/assets/f373252a-1d2b-4f9b-ac68-a5a428262213" />

105 In that file find ost-sampleconfig.php

<img width="1440" alt="OST_123" src="https://github.com/user-attachments/assets/425fe263-5f67-4d79-ae9a-d28dbe3fca78" />

106 Right click ost-sampleconfig.php and rename it to "ost-config.php". 

<img width="1440" alt="OST_124" src="https://github.com/user-attachments/assets/907d5204-63e6-46f7-a96b-b79b52cf94b3" />

107 Make sure there are NO errors in the name. 

<img width="1440" alt="OST_125" src="https://github.com/user-attachments/assets/050b3fb9-646f-4b24-835b-41ad3fb4ca45" />

108 Now you need to assign permissions to ost-config.php
    Right click ost-config.php and click properties 

<img width="1440" alt="OST_126" src="https://github.com/user-attachments/assets/1d38e4ca-e1b1-47c3-b06f-5fcfac354f78" />

109 From there go to Security and then to Advance. 

<img width="1440" alt="OST_127" src="https://github.com/user-attachments/assets/906731f7-c5c0-4905-9ac4-933cbc621530" />

110 Click "Disable inheritance" and "Remove all inherited permissions from this object".

<img width="1440" alt="OST_128" src="https://github.com/user-attachments/assets/14960bb6-cf71-4cf8-8306-06a5b37e9f7e" />

111 From there click "Add". 

<img width="1440" alt="OST_129" src="https://github.com/user-attachments/assets/deda4a36-c3fb-4079-9918-a217ef5031d8" />

112 Click "Select a principal"

<img width="1440" alt="OST_130" src="https://github.com/user-attachments/assets/df1ae14a-6068-40e0-979e-ba02233e4a65" />

113 For object name type "Everyone", click "Check Name" and "OK". 

<img width="1440" alt="OST_131" src="https://github.com/user-attachments/assets/16197915-eb16-4e66-b352-3cf3ba1c815f" />

114 Ceck Full control and click ok. 

<img width="1440" alt="OST_133" src="https://github.com/user-attachments/assets/c6c6df4c-72ad-4813-b081-ddbe39c25148" />

115 Your permission entries should look like this. As long as it does click Apply.

<img width="1440" alt="OST_135" src="https://github.com/user-attachments/assets/975bf9b4-5c70-4857-bd53-3c7c2c7a2801" />

116 Click OK for ost-config.php Properties. 

<img width="1440" alt="OST_137" src="https://github.com/user-attachments/assets/c45f3a2c-8b42-44b1-a525-4ace40c55b7a" />

117 Go back to the osTicket Website and click Continue at the bottom. 

<img width="1440" alt="OST_138" src="https://github.com/user-attachments/assets/26216979-4088-406e-8759-51a7977dea4d" />

118 Now fill out the information for Helpdesk Name: and Default email. )This information doesn't need to be specific.)

<img width="1440" alt="OST_139" src="https://github.com/user-attachments/assets/898a1de2-f0e3-46c5-839b-34c68ffd9d7c" />
 
119 Fill out the following information as well. This can also be anything but the email addresses do need to be different. 
    Next you need to log into the MySQL database. 

<img width="1440" alt="OST_140" src="https://github.com/user-attachments/assets/bcf18614-2911-49bd-b0ae-2c3e776a3b69" />

120 Go back to osTicket-Installation-Files

<img width="1440" alt="OST_141" src="https://github.com/user-attachments/assets/b3630832-3e77-43cd-a0e5-c04fdf8d8479" />

121 Open HeidiSQL_12.3.0.6589_Setup

<img width="1440" alt="OST_142" src="https://github.com/user-attachments/assets/d9d2a3f8-d63d-402c-8723-2b8b10aadf21" />

122 Accept the aggreement and click next. 

<img width="1440" alt="OST_143" src="https://github.com/user-attachments/assets/03ccda87-ad84-4a1f-86cc-1660b5bc410b" />

123 Next 

<img width="1440" alt="OST_144" src="https://github.com/user-attachments/assets/21d9168d-7ac0-4271-b9a1-f4354a0a8ac1" />

124 Next 

<img width="1440" alt="OST_145" src="https://github.com/user-attachments/assets/25d0bd75-bdc3-4723-a7b3-917955ed8e69" />

125 Install 

<img width="1440" alt="OST_146" src="https://github.com/user-attachments/assets/a2743d85-6582-4ea6-b3d9-9b148371e078" />

126 Check the Launch HeidSQL box is checked then click finish. 

<img width="1440" alt="OST_147" src="https://github.com/user-attachments/assets/0b8aaab9-e9bc-468b-9077-8247ebc8b6c4" />

127 Skip

<img width="1440" alt="OST_148" src="https://github.com/user-attachments/assets/79b8f9d5-29ee-46b1-8b7b-9dc622ebca03" />

128 In the session manager click new 

<img width="1440" alt="OST_149" src="https://github.com/user-attachments/assets/95b70e91-7946-4d8c-a3be-0547aa194eed" />

129 Now put in the User: and Password: you created and press Open. 

<img width="1440" alt="OST_150" src="https://github.com/user-attachments/assets/c4ff9948-3150-4938-963d-d0f2c4d030d3" />

130 Right click Unnamed, click Create New, and then Database. 

<img width="1440" alt="OST_152" src="https://github.com/user-attachments/assets/28f537c2-59b0-499c-a08e-86e5c0a58724" />

131 The name needs to be exactly "osTicket" then click OK. 

<img width="1440" alt="OST_153" src="https://github.com/user-attachments/assets/11fe5d79-479e-4812-926a-e0b589273220" />

132 Now you can see that it was created and will be utilized later on. 

<img width="1440" alt="OST_154" src="https://github.com/user-attachments/assets/ed42e509-9f4e-41f1-aec0-e1feb3a2ae1f" />

133 Back on the osTicket webpage in the Database Settings secction fill out the remaining information. 
    MySQL: Database 
    MySQL: Username 
    MySQL: Password
    Then Install now 

<img width="1440" alt="OST_155" src="https://github.com/user-attachments/assets/84d6ca1e-758d-42e6-ab51-e8972a65f18d" />

135 After the installation you will be shown this screen showing it was successfull.

<img width="1440" alt="OST_157" src="https://github.com/user-attachments/assets/e7237cc9-4758-4112-bb09-32127a706788" />

136 If you want to check go back into HeidiSQL right click osTicket and click refresh. 
    This will show all the different tables that were created in the database. 

<img width="1440" alt="OST_158" src="https://github.com/user-attachments/assets/be547c4a-12c0-415b-a1cf-3e1df0c15182" />

138 This link http://localhost/osTicket/scp/login.php will take you to the log in page to sign in under different users. 
    Try loging in as admin and with the password created earlier. 

<img width="1440" alt="OST_161" src="https://github.com/user-attachments/assets/68c3207c-bd35-4c01-95ed-aec035b05764" />

139 There is one ticket created (the install ticket) but this you will view and hand tickets. 

<img width="1440" alt="OST_162" src="https://github.com/user-attachments/assets/ce7854b1-d239-462a-b425-c39ed963c5a2" />

141 This link http://localhost/osTicket/ will take you to the page to sign in and submit tickets as a user.

<img width="1440" alt="OST_166" src="https://github.com/user-attachments/assets/c9152c8b-2554-4b61-96c9-64bbe0de0ddf" />
