# ForensicsToolkit
Name: OSXpmem
Description: OSXpmem is a memory collection tool for OSX operating system.  The project is open source on Github.
Your personal review
Good tool, easy to use and seems to work well
Your personal notes on usage
 Change permissions of the application so it can be run:
  o Chown -R root:wheel osxpmem.app/
 Change into the osxpmem.app directory:
  o Cd /osxpmem.app
 Run the application to collect memory from the system:
  o ./osxpmem.app/osxpmem -o <output_dir>
  o This command will output a .aff4 volume file, which can then be analyzed with
osxpmem or various other memory analysis tools
Source URL (if applicable)
https://github.com/google/rekall/releases

Name:Wireshark
Description: Wireshark is a packet analysis tool.  It is used in conjunction with a npcap to capture and analyze traffic
Your personal review:  Wireshark is great.  It is super easy to use and analyze what is going on in the packets
Your personal notes on usage
not many notes on this, you can just browse the pcaps.  TCP trace is probably my favorite functionality.
Source URL (if applicable)
https://www.wireshark.org/download.html

Name:FTK toolkit
Description:  A utah based toolkit that is used for digital forensics.  It is not free.  It includes a variety of tools, including FTK imager which can be used to obtain an image of a hard drive.
Your personal review: FTK imager is really good.  I wasn't able to use it to its full potential, but it seems like it has a lot of capabilities that are very useful.
Your personal notes on usage
Everything I used on it was GUI based and pretty self explanatory
Source URL (if applicable)
https://accessdata.com/product-download/ftk-imager-version-4-3-0

Name: Netcat
Description
Your personal review
Your personal notes on usage
set up listener: nc -l -p [port]
netcat cheat sheet: https://www.sans.org/security-resources/sec560/netcat_cheat_sheet_v1.pdf
Source URL (if applicable)
https://sourceforge.net/projects/nc110/

Name: 7zip
Description.  7zip is a tool used for compressing and decompressing files.
Your personal review:
Best Zipping tool I have used.
Your personal notes on usage:
right click and go to 7zip in the options to see capabilities
Source URL (if applicable)
https://www.7-zip.org/download.html

Name: LiME
Description:  This is a Linux memory acquisition tool.  It is open source.
Your personal review:  I wasn't entirely impressed with this tool.  I had issues getting it to work, especially over netcat.
Your personal notes on usage:
first, run the make file, then
insmod ./lime.ko "path=<outfile | tcp:<port>> format=<raw|padded|lime> [digest=<digest>] [dio=<0|1>]"
Source URL (if applicable)
https://github.com/504ensicsLabs/LiME

Name: Dd
Description: DD is a disk cloning tool that can be used for Linux.
Your personal review
I had issues with DD.  Something caused it to freeze at the same point of taking an image everytime I tried.  This made the tool unusable for me, and I wasn't able to resolve this issue.  for this reason I am not a fan of DD.
Your personal notes on usage
cloning a drive:  dd if=/dev/rdsk/device-name of=/dev/rdsk/device-name bs=blocksize
Source URL (if applicable)

Name: Volatility
Description: Volatility is a tool that is used for analysis of memroy captured from a system.  It can do a lot of different things, including pulling network traffic and searching for malware.
Your personal review:  Great tool.  It is super slick, and definitely something I will use int the future.
Your personal notes on usage:
Process scan: volatility -f lab.vmem --profile=WinXPSP2x86 psscan
Process tree: volatility -f lab.vmem --profile=WinXPSP2x86 pstree
dump potential malware: volatility -f lab.vmem --profile=WinXPSP2x86 malfind --dumpdir /home/root
see below for command reference:
https://github.com/volatilityfoundation/volatility/wiki/Command-Reference
Source URL (if applicable)
https://github.com/volatilityfoundation

Name: autopsy
Description: tool, similar to FTK, that can be used to analyze drive images to find files and other info.
Your personal review:  Good tool, unfortunately I didn't use it much as I primarily used FTK.  From what I saw it seemed about equally as good.
Your personal notes on usage
NA, mostly GUI based
Source URL (if applicable)
https://www.autopsy.com/download/

Name: Radare2
Description:  disassembler/assembler used for analyzing assembly code of malware and other programs.
Your personal review:  Awesome tool.  I've used a few others, including GDB, and this one is by far my favorite.
Your personal notes on usage
Run Radare2 with the executable: r2 lab110x00.exe
Analyzed the file to output assembly:  pdf@main
The below link details how to edit assembly in Radare2
https://rayoflightz.github.io/linux/assembly/2019/03/26/Binary-patching-using-radare2.html
Source URL (if applicable)
https://rada.re/n/
