# Remote-Shutdown-libcurl-jsoncpp

Subsystem: Windows

<b>Setup</b>: <br></br>
  libcurl:
  - Download curl: https://curl.haxx.se/download/curl-7.70.0.zip
  - Open Developer Command Prompt for Visual Studio 2019 -> Go to this directory -> C:\curl\winbuild\
  - Run nmake /f Makefile.vc mode=static. This will build curl as a static library into C:\curl\builds\libcurl-vc-x86-release-static-ipv6-sspi-winssl\
  - Create a new project in Visual Studio 2019
  - Project Properties -> VC++ Directories -> Include Directories add C:\curl\builds\libcurl-vc-x86-release-static-ipv6-sspi-winssl\include\
  - Project Properties -> VC++ Directories -> Library Directories add C:\curl\builds\libcurl-vc-x86-release-static-ipv6-sspi-winssl\lib\ there
  - Project Properties -> Linker -> Input -> Additional Dependencies add libcurl_a.lib, Ws2_32.lib, Crypt32.lib, Wldap32.lib and Normaliz.lib
  
  
  
  jsoncpp:
  - Download jsoncpp: https://sourceforge.net/projects/jsoncpp/
  - Copy lib and include directory to your repository
  - Project Properties -> C/C++ -> Additional Include Directories -> Add the include file in jsoncpp
  - Go to jsoncpp -> src -> lib_json -> copy all the files and paste it on the same directory with app or main.cpp
  - Solution Explorer -> right click Source Files -> Add existing item -> Add all the pasted items from lib_json

   <b>Happy compiling</b>
