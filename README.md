# CUSTOM Minispy File System Minifilter Driver

Proje kapsamında Microsoft'un [MINISPY](https://github.com/microsoft/Windows-driver-samples/tree/main/filesys/miniFilter/minispy) minifilter örneği alınarak üzerinde ihtiyaçlara uygun değişiklikler yapılmıştır.
Yapılan değişiklikler sonrasında:
- Kullanıcı **MOVE** ve **RENAME** işlemleri hakkında bilgilendirilmektedir.
- **DELETE** işlemi engellenebilmektedir.
- Dosya dinleme işlemi belirlenen path özelinde yapılabilmektedir.


#  Prerequisites
1. Operating System
Windows 10 or later (for development and testing)

2. Tools
Visual Studio (2019 or later)\
Windows Driver Kit (WDK) matching your Visual Studio version

3. Administrator privilege to install/load drivers.

# Setup
1. Clone the project:\
  `git clone https://github.com/betulyaman/minispy-custom.git`

2. Open the solution **minispy.sln** in Visual Studio and build.

3. Install and load the minifilter:\
Go to installation directory: `cd ...\minispy\filter\x64\Debug\minispy`\
Right click to `minispy.inf` and select **install**.\
Open cmd as an administrator.\
run `fltmc load minispy` to load the minifilter.\
run `fltmc attach minispy <volume>:` to attach the minifilter to \<volume\>.


6. Run user application \
Go to user applicaiton directory: `cd D:\workspace\minispy\user\x64\Debug`. \
run `minispy.exe` as an **administrator**.


# SCREEN DUMPS
1. START \
![start](https://github.com/user-attachments/assets/e3d3159c-58d7-457f-b2c9-b029738df1dc)

2. MOVE \
![move](https://github.com/user-attachments/assets/ee979772-c61e-40f0-bc18-5cf22644361b) \

3. RENAME \
![rename](https://github.com/user-attachments/assets/3ca50434-3d72-422d-93dd-d5449dbcffee)

4. DELETE \
 ![delete](https://github.com/user-attachments/assets/37ac11be-2322-4c23-b16f-94bc5cc2b39e)
