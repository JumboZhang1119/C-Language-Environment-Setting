C-Language Environment Setting with VS code on Windows
====
How to build your first C-Language environment setting on Windows with VS Code.
<br>
<br>
## For Windows user:
To build your C-Language environment, we can roughly divide the steps into the following 5 steps:
<br>
* Download VS Code
* Download MinGW-W64
* Download LLVM
* Other setting
* Begin your first code

### Download VS Code
1. Go to [VS Code official website](https://code.visualstudio.com/) and click `Download for Windows`, then it will download automatically. <br><br>
![01](https://user-images.githubusercontent.com/107752584/174463881-7f42e5d6-2df9-4e36-9922-bfe0468876f8.png)<br><br>
2. Go to your download folder and open `VSCodeUserSetup-x64.exe`, then follow these steps to install VS Code. <br><br>
![02](https://user-images.githubusercontent.com/107752584/174464162-2b4cba09-bc6d-4443-8a85-0c4bbcc52e89.png)<br>
![03](https://user-images.githubusercontent.com/107752584/174464229-b8b25934-21e7-4358-8c11-b210e49919cb.png)<br>
![04](https://user-images.githubusercontent.com/107752584/174464253-29a1a987-46e1-46e9-bedb-d373e43a802d.png)<br><br>

### Download MinGW-W64
3. Go to [MinGW-SourceForge](https://sourceforge.net/projects/mingw-w64/) and choose `Files` tab.<br><br>
![05](https://user-images.githubusercontent.com/107752584/174464780-5905f2ad-04dc-4262-96bb-ec4ea4e2234e.png)<br><br>
4. Scroll down to find out `x86_64-posix-seh`and click to download. <br><br>
![06](https://user-images.githubusercontent.com/107752584/174464832-67556881-760b-4ec2-8067-13b9aea62342.png)<br><br>
5. Extract the downloaded file and move `mingw64` of the file to `C:\Program Files (x86)` , then go to `C:\Program Files (x86)\mingw64\bin` and clone the path.<br><br>
![07](https://user-images.githubusercontent.com/107752584/174466273-81295689-e5d2-42d4-9121-d22d7574c62d.png)<br><br>
6. Open your system setting and find out `System information`, then choose `Advanced system setting`.<br><br>
![08](https://user-images.githubusercontent.com/107752584/174465960-bd202336-bb06-4079-93c1-de88edaf39af.png)<br>
![09](https://user-images.githubusercontent.com/107752584/174465966-a7c6f61e-114d-4b2d-b2f2-db2b9332ee97.png)<br><br>
7. Open `Environment variable` window under `Advance tab`, and click `Path` in `System virable`, then click `Edit`.<br><br>
![10](https://user-images.githubusercontent.com/107752584/174465968-9c10e7b6-8bbe-407f-9743-75b80c5b9fd1.png)<br>
![11](https://user-images.githubusercontent.com/107752584/174465970-e6952632-b182-48d4-842f-f9dbd1b2e5c5.png)<br><br>
8. Add a `new path` in it and paste the path you cloned at `step 5`, then click certain to close all windows we opened at step 6-8.<br><br>
![12](https://user-images.githubusercontent.com/107752584/174465971-41f4d341-497c-4a81-946d-505cf05c68bc.png)<br><br>

### Download LLVM
9. Go to [LLVM Download Page](https://releases.llvm.org/download.html) and click `page` of latest version, then scroll down to find out `LLVM-"your version"-win64.exe` and click to download it.<br><br>
![13](https://user-images.githubusercontent.com/107752584/174466633-b32c6d11-6e65-40ae-9a25-7da0168f09cb.png)<br>
![14](https://user-images.githubusercontent.com/107752584/174466634-2c7f0e60-9914-4ec5-983f-554338b8748c.png)<br><br>
10. Double click the `LLVM-"your version"-win64.exe` to perform installation.<br><br>
![15](https://user-images.githubusercontent.com/107752584/174467816-cb62a84e-ec06-49a4-afa2-0762f047c070.png)<br>
![16](https://user-images.githubusercontent.com/107752584/174467817-e7743470-d961-49d8-9659-2d3bdc884fc6.png)<br><br>
11. Change the option from `Do not add LLVM to the system PATH` to `Add LLVM to the system PATH for all users`.<br><br>
![17](https://user-images.githubusercontent.com/107752584/174467818-b984355f-a7ff-4f94-9a6f-2a358977fd14.png)<br><br>
12. Change the default path from `C:\Program Files (x86)\LLVM` to `C:\LLVM`, then continue to install.<br><br>
![18](https://user-images.githubusercontent.com/107752584/174467819-fb1e8f91-c7a3-488f-b107-ce53c2fe0500.png)<br>
![19](https://user-images.githubusercontent.com/107752584/174467821-9a409130-a410-4d01-a2f1-234869d426df.png)<br>
![20](https://user-images.githubusercontent.com/107752584/174467823-e9d66272-eea1-4a4f-9162-6ee38bd66baf.png)<br><br>
13. Go to `C:\Program Files (x86)\mingw64` then copy all folders.<br><br>
![21](https://user-images.githubusercontent.com/107752584/174468249-8e73111a-ef76-4704-8efb-708cb3f25c38.png)<br><br>
14. Go to `C:\LLVM` and paste all files we copied at step 13 in it.<br><br>
![22](https://user-images.githubusercontent.com/107752584/174468316-30a9278f-3894-4143-91ad-c39015cec698.png)<br><br>
15. To make sure we have successfully installed MinGW and LLVM, press `Win + R` then enter `powershell`.<br><br>
![23](https://user-images.githubusercontent.com/107752584/174468568-b52ac0a6-1a73-49d4-bb32-9d6382bda1b9.png)<br><br>
16. Enter following codes in powershell to know weather your installation is successful (You can also do this in CMD):<br>
```
gcc --version
```
```
clang --version
```
If your powershell also produces the following result, congratulations you are very close to success.<br>
If not, try following the steps above carefully again.<br><br>
![24](https://user-images.githubusercontent.com/107752584/174468839-cfc10853-a3d6-4db8-94c9-b6e2231815b6.png)<br><br>

### Other setting
17. Open `VS Code App`, and click `Extensions` at the left side. Search `C/C++`, `C++ Intellisense`, `C/C++ Extension Pack`, `Code Runner` and download separately.<br><br>
![25](https://user-images.githubusercontent.com/107752584/174469567-21c04861-82f0-4325-a150-47f780bbdb77.png)<br>
![26](https://user-images.githubusercontent.com/107752584/174469568-3c98185d-4461-473b-8253-2a4823774b21.png)<br>
![27](https://user-images.githubusercontent.com/107752584/174469569-39fe66ec-2843-4225-a58f-05c555340d3b.png)<br>
![28](https://user-images.githubusercontent.com/107752584/174469611-da91c529-6a5e-4651-9adf-6355e24e1fc6.png)<br><br>
19. Go to wherever you prefer to put your code in (For me I create a folder `C` at `D:\Coding`), then create another new folder `.vscode` in it.<br><br>
![29](https://user-images.githubusercontent.com/107752584/174469660-b6c76f6d-f589-479c-bdec-923985f505b5.png)<br><br>
20. Open the `.vscode` folder you create in step 19, then paste the 4 files (I have attached them in the above repository.) in. <br><br>
![30](https://user-images.githubusercontent.com/107752584/174469964-14ff2a8f-4caa-4329-8a3c-ae29e2f6cded.png)<br><br>
20. In `VS Code App` click `File` > `Open Folder` and choose your folder (For me, I choose my `C` folder established at step 19).<br><br>
![31](https://user-images.githubusercontent.com/107752584/174470196-383916dd-08b8-4143-a772-545ee0bd9b3a.png)<br><br>
21. Create a new file and named `XXXX.c (or XXXX.cpp)`.<br><br>
![32](https://user-images.githubusercontent.com/107752584/174470336-c467627e-1481-4762-8ecb-392c3acc839e.png)<br><br>
22. Go to your `.vscode` folder and find out your `XXXX.c (or XXXX.cpp)` file, then move it from `.vscode` to `your folder`(For me is `C`).<br><br>
![33](https://user-images.githubusercontent.com/107752584/174471047-32db2c41-6846-4758-abfa-b8db4d1a3d33.png)<br>
![34](https://user-images.githubusercontent.com/107752584/174471049-f3f6d519-7a09-475e-afff-ec9cb674418e.png)<br><br>

### Begin your first code!
23. You can try "Hello world!" for your first code!
```
#include <stdio.h>
int main() {
    printf("Hello World");
    return 0;
}
```
![35](https://user-images.githubusercontent.com/107752584/174471304-1cc025ee-2858-4950-877c-9b5e413665a3.png)<br><br>
24. Then click `File` > `Auto Save`, and press `Ctrl + Alt + N` to run the code.<br><br>
![36](https://user-images.githubusercontent.com/107752584/174471427-1932f79f-b34f-41cb-b585-9d21c5de3a65.png)
## That's all!
