
## MITRE Mapping

###  Observed

- T1486 – Data Encrypted for Impact (with **.arachna** extension)
- T1567.002 – Exfiltration to Cloud Storage (**Mediafire**)
- T1005 – Data from Local System (**TallyPrime** Logs)
- T1083 – File and Directory Discovery (**TallyPrime** Logs)
- T1586.002 – Compromise Accounts: Email Accounts (Arachna_Recovery@firemail.de)
- T1056.003 – Input Capture: Web Credential Harvesting (Credential scraping behavior if the leaked files are opened in a browser)
- T1583.001 – Acquire Infrastructure: **Botnets** (Simultaneous automated login attempts consistent with botnet-driven credential abuse)
- T1078 – Valid Accounts

###   Inferred

- T1133 – Phishing (Attachment / Link)
- T1566.001/T1566.002 – Phishing (Attachment / Link)
- T1190 – Exploit Public-Facing Application
- T1059.003 – Windows Command Shell
- T1204.002 – User Execution: Malicious File
- T1547.001 – Registry Run Keys / Startup Folder
- T1053.005 – Scheduled Task
- T1068 - Exploitation for Privilege Escalation
- T1562.001 - Disable or Modify Security Tools
- T1027 - Obfuscated Files or Information
- T1555 – Credentials from Password Stores
- T1110 – Brute Force
- T1021.001 – Remote Services: RDP
- T1021.002 – SMB/Windows Admin Shares
- T1041 – Exfiltration Over Command and Control Channel
- T1020 – Automated Exfiltration



###### The **Arachna ransomware** exhibits strong structural and behavioral correlation with the **Dharma (Crysis) ransomware family**. Since **2020**, Dharma’s core developers have operated it as a **Ransomware-as-a-Service (RaaS)** platform, enabling a wide range of independent affiliates to deploy customized variants using the same underlying builder. Public threat-intelligence reporting and large-scale sample analysis have identified numerous Dharma-family offshoots over time, including **Gnik, K1ng, Zxcvb, Watch, 62IX, BlackBit, and Polis**, among others. These variants consistently reuse Dharma’s hallmark characteristics—file-renaming conventions incorporating victim IDs and contact emails, standardized ransom workflows offering limited free decryption, and similar extortion messaging. The naming scheme, ransom instructions, and operational patterns observed in Arachna align closely with this established Dharma affiliate ecosystem, indicating that **Arachna is most likely a forked Dharma builder operated by an independent RaaS affiliate.**


### Ransom Note Comparison

##### Arachna

All your files have been encrypted! All your files have been encrypted due to a security problem with your PC. If you want to restore them, write us to the e-mail Arachna_Recovery@firemail.de You have to pay for decryption in Bitcoins. The price depends on how fast you write to us. After payment we will send you the decryption tool that will decrypt all your files. Free decryption as guarantee Before payment you can send us 2 files for free decryption. Please note that files must NOT contain valuable information. The file size should not exceed 1MB. As evidence, we can decrypt one file How to obtain Bitcoins The easiest way to buy bitcoins is LocalBitcoins site. You have to register, click ‘Buy bitcoins’, and select the seller by payment method and price. hxxps://localbitcoins.net/buy_bitcoins Also you can find other places to buy Bitcoins and beginners guide here: hxxp://www.coindesk.com/information/how-can-i-buy-bitcoins/ Attention! Do not rename encrypted files Do not try to decrypt your data using third party software, it may cause permanent data loss Decryptors of other users are unique and will not fit your files and use of those will result in a loose of data.

##### Dharma

All your files have been encrypted! All your files have been encrypted due to a security problem with your PC. If you want to restore them, write us to the e-mail moremo123123@cock.li Write this ID in the title of your message [snip] In case of no answer in 24 hours write us to theese e-mails: moremo123123@cock.li You have to pay for decryption in Bitcoins. The price depends on how fast you write to us. After payment we will send you the decryption tool that will decrypt all your files. Free decryption as guarantee Before paying you can send us up to 5 files for free decryption. The total size of files must be less than 10Mb (non archived), and files should not contain valuable information. (databases,backups, large excel sheets, etc.) How to obtain Bitcoins The easiest way to buy bitcoins is LocalBitcoins site. You have to register, click 'Buy bitcoins', and select the seller by payment method and price. https://localbitcoins.com/buy_bitcoins Also you can find other places to buy Bitcoins and beginners guide here: http://www.coindesk.com/information/how-can-i-buy-bitcoins/ Attention! Do not rename encrypted files. Do not try to decrypt your data using third party software, it may cause permanent data loss. Decryption of your files with the help of third parties may cause increased price (they add their fee to our) or you can become a victim of a scam.

## IoCs

#### File Format + Extension
###### Dharma →  `file.jpg[id-XXXXXX].[SupportForYou@india.com].dharma (File Name + Email + Extension)

###### Arachna →  `file.jpg[id-XXXXXX].[Arachna_Recovery@firemail.de].Arachna (File Name + Email + Extension)


### Mechanism 

- ##### Two free decryptions
- ##### Same two file - free decryptions for sample
- ##### Email only decryption
- ##### Wording to avoid third party decrypters
- ##### Same Note Layout
- ##### Same “Restore” helper file
  
  
###  Target Profile

- ##### TallyPrime Users
- ##### GST invoice workflows
- ##### Small e‑commerce
- ##### Clinics & healthcare
- ##### Real estate shops
- ##### Supply chain firms
  
####   Decryption communication Channel

The group associated with Arachna relies on privacy-oriented email providers such as **firemail.de** (and similar services historically favored by Dharma affiliates, including Tutanota). These providers offer encrypted mail transport and limited publicly documented metadata retention, making attribution via email infrastructure alone inherently difficult.

