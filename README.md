# Anti-varus

The misspelling of anti-virus is deliberate, this is a project to further understand how antivirus software works, not replicate a real AV. I wouldn't want anyone use this software expecting a real antivirus.

## Alternative working AV software

| Windows                                       | Linux                              |
|-----------------------------------------------|------------------------------------|
| [Malwarebytes](https://www.malwarebytes.com/) | [ClamAV](https://www.clamav.net/)  |
| [Sophos](https://home.sophos.com/en-us)       |                                    |
| [Kaspersky](https://www.kaspersky.co.uk/)     |                                    |
| [Bitdefender](https://www.bitdefender.co.uk/) |                                    |

Blog post: TBD

## Compilation  

You will need Golang installed  
Open Bash  
Download the code to your Downloads folder (unzip the code)  
<code>wget https://github.com/ScioShield/anti-varus-linux.git -P ~/Downloads</code>  
Open the downloads folder  
<code>wget -O ~/Downloads/anti-varus.zip https://github.com/ScioShield/anti-varus-linux/archive/refs/heads/master.zip</code>  
Unzip the file  
<code>unzip ~/Downloads/anti-varus.zip -d ~/Downloads</code>  
Open the dir  
<code>cd ~/Downloads/anti-varus-linux-master</code>  
Copy the .vdb file to where it needs to be  
<code>cp varus.vdb /tmp/</code>  
Compile the go package  
<code>go build anti-varus-linux.go</code>  
Run the code  
```
╭─scio@shield ~/Downloads/anti-varus-linux-master 
╰─$ ./anti-varus-linux 
Enter what file you would like to scan (full path and filename):
/home/scio/Downloads/anti-varus-linux-master/varus.vdb
Match found!
Target hex: 3731373736353732373437396161
Target string: 717765727479aa
Target file: /home/scio/Downloads/anti-varus-linux-master/varus.vdb
File SHA256 Hash is: ed99d22d63e71f29065929d608851e593b40697293c4701de53ecd073e5cc293  /home/ghost/Downloads/anti-varus-linux-master/varus.vdb
```  

Do not run the code against large files!    
