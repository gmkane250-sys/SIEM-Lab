# SIEM-Lab
Description
This lab is a demonstration of my abilities to set up a SIEM application across a network. I have two virtual machines connected on a network through the VMware hypervisor. One machine is a Kali-Linux which represents the security manager. The other machine represents a employee/worker with a sensitive file that needs to be monitored by the management machine. The wazuh SIEM and XDR is implimented on both machines. Documented later is proof of the SIEM operating as well.
Table of Contents

# Setting up the virtual machines
<img width="1804" height="759" alt="image" src="https://github.com/user-attachments/assets/f40ee859-54e3-46d9-9a76-cd87f919924e" />
Figure 1: VMware's website where I download the hypervisor

<img width="1834" height="997" alt="image4" src="https://github.com/user-attachments/assets/36d9b002-3084-4d56-a442-e0f397da039e" />
Figure 2: Grabbing the latest release of the hypervisor after clicking the downlaod link

<img width="1803" height="998" alt="image2" src="https://github.com/user-attachments/assets/0593dd85-c9db-4c43-804f-b8c795a6700d" />
Figure 3: Downloading the Kali Linux compatible with VMware

<img width="1834" height="997" alt="image4" src="https://github.com/user-attachments/assets/53e6dbfe-ee26-4595-838d-ffb753435982" />
Figure 4: Extracting the files from the zip

<img width="1777" height="964" alt="image5" src="https://github.com/user-attachments/assets/d50b332d-3294-46c2-850d-0a5b328580de" /><img width="1838" height="981" alt="image7" src="https://github.com/user-attachments/assets/1111a1ba-6663-4ea9-a1ce-030eb515f9b7" />
Figures 5 and 6: The virtual machine's file and then the virtual machine implemented into the VMware hypervisor

<img width="1278" height="823" alt="image8" src="https://github.com/user-attachments/assets/032efcbc-57c9-403f-ad2d-e61eed9c2df7" />
Figure 7: Command line to fully update kali

<img width="1828" height="958" alt="image9" src="https://github.com/user-attachments/assets/58301119-c02d-4d0b-a36b-4deeb8085427" />
Figure 8: Grabbing the Windows 11 iso file free on their website

<img width="993" height="743" alt="image10" src="https://github.com/user-attachments/assets/dd473c7b-e192-4f91-82de-87a483063a92" />
Figure 9: Booting up the windows machine after plugging in the iso file

# Setting up the SIEM
<img width="1817" height="1020" alt="image11" src="https://github.com/user-attachments/assets/74489e2d-b145-49b8-b1c9-b9e89e27b20c" />
Figure 10: Wazuh's website with the agent/worker download as well as the manager downlaod and installation guide

<img width="1473" height="915" alt="image12" src="https://github.com/user-attachments/assets/9a4d65e3-a413-4d0f-b1d3-b60615865adb" />
Figure 11: Using the installation command given by their guide for the manager software onto the linux machine

<img width="1282" height="850" alt="image13" src="https://github.com/user-attachments/assets/22e1c91d-173a-4089-8b52-3e0cbfcbad4c" />
Figure 12: Downloading the agent software onto the windows machine

<img width="1036" height="667" alt="image14" src="https://github.com/user-attachments/assets/a2384b46-885a-4841-8eba-b6e220b871b2" />
Figure 13: Grabbing my ip address for the manager. As well as inputting a command to pull up the agent manager

<img width="1219" height="835" alt="image15" src="https://github.com/user-attachments/assets/0bbcf9ea-6dd2-4010-86e3-c18112e0e160" />
Figure 14: Putting the ip address of the agent into the software as well as naming the agent

<img width="1286" height="859" alt="image17" src="https://github.com/user-attachments/assets/bfec2795-ffd7-42d8-b981-54421f3e4321" />
Figure 15: Grabbing the key for the agent

<img width="645" height="513" alt="image16" src="https://github.com/user-attachments/assets/2bfd55be-2f1f-4203-82b0-2e2a62bac48f" />
Figure 16: Putting in the manager's ip as well as the extracted key to activate the agent software

<img width="1276" height="850" alt="image20" src="https://github.com/user-attachments/assets/a1feec4e-8578-4e27-a5e0-4b74d388cb08" />
Figure 17: The active agent on the manager's screen

<img width="877" height="689" alt="image21" src="https://github.com/user-attachments/assets/b9061263-37ed-4337-94c5-f4fd3fea70f0" />
Figure 18: Entering the view configs file to edit the software and add a sensitve file for file integrity monitoring

<img width="1011" height="707" alt="image22" src="https://github.com/user-attachments/assets/bd273676-fa92-41b8-8b28-1e3ecf65e7ba" />
Figure 19: Adding the path to the configs file to ensure the sensitve file is monitored

# Proof it works
<img width="1270" height="798" alt="image23" src="https://github.com/user-attachments/assets/ef06b8e4-91ac-441f-8bd4-4255c44b501a" />
Figure 20: File integrity monitoring after setup, but before tampering. Blank as it should be.

<img width="956" height="672" alt="image24" src="https://github.com/user-attachments/assets/435e5181-8391-48bd-8c89-66ff76f17952" />
Figure 21: Adding a new file, thus tampering with the integrity of the file on the worker's computer.

<img width="1270" height="819" alt="image25" src="https://github.com/user-attachments/assets/3f7ea2f6-e924-40e2-a16f-dcc769cc99c9" />
Figure 22: File integrity monitoring after tampering. Tampering detected!
