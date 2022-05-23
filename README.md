# omfe-cpp
This is OMFE AES, a powerful file encryption/decryption tool which uses AES 256 CBC/ECB algorithm. It is written entirely in c++. Unlike a basic single file encryption, this tool operates on multiple files and folders and retains the folder structure which is targeted by the application. Meaning all sub-folders under a target folder maintains the original structure. This is a command line tool, not a GUI.

`Note:` This tool use multi-threading while operating on files. This is not a destructive program in any manner. It neither creates unnecessary files nor deletes any files. The tool is absolutely safe and it works on any type of machine. The author only distributes compiled executable and not source files. There is no need to make and install.

`For Windows users:`
  You need to download omfe.exe and cygwin1.dll in one location. omfe.exe won't run without cygwin1.dll.

`How it works?`
  1. To encrypt, create a folder named “decrypt” where ever you like on the file system.
  2. Move all the files and folder into this “decrypt” folder.
  3. Run the application omfe.exe with command line arguments. To find the command line arguments type “omfe.exe  --help”.
  4. To decrypt, follow the same process as encrypt but in reverse.

example: 

Check this path in windows. I have created a folder named 'decrypt' and it contains this directory structure
![image](https://user-images.githubusercontent.com/40391497/169683897-d86f0dd9-10f2-4585-9310-6d88af3c9875.png)


I run this command `omfe.exe enc -k 12121212121212121212121212121212 -iv 10101010101010101010101010101010 -m cbc -s 128 C:\Users\DELL\Music\some_folder`. Note all options tags are optional except the folderpath. This is what you will get.

![image](https://user-images.githubusercontent.com/40391497/169684129-1db8fd77-fc8a-40d1-9015-da743ff28151.png)

You can safely delete the "decrypt" folder. When you want to decrypt, just pass the same command as passed for encrypt but with `dec` argument, like this `omfe.exe dec -k 12121212121212121212121212121212 -iv 10101010101010101010101010101010 -m cbc -s 128 C:\Users\DELL\Music\some_folder`

This tool is extremely fast as it is written in C++. For java version check my https://github.com/leogitpub/OMFE repository.

Star this project if you used it and liked it.

sha256 checksum of this tool omfe.exe => fb0a7f780b7eda09318ee4611cf2654bdc923315e7f72c073dd1733044f7ebc9

cygwin1.dll checksum => 6ad6c03ac893bce8aeb65362c7615b7c74d457276ce6bdcde40a110178267fa3

cygstdc++-6.dll checksum => c883d557d5fef43a6ea031bf48c50e42feecbc6621c85ec6a3ee334220345f32
