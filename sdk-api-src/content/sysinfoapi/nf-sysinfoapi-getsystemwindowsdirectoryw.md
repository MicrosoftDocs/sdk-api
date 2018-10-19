---
UID: NF:sysinfoapi.GetSystemWindowsDirectoryW
title: GetSystemWindowsDirectoryW function
author: windows-sdk-content
description: Retrieves the path of the shared Windows directory on a multi-user system.
old-location: base\getsystemwindowsdirectory.htm
tech.root: sysinfo
ms.assetid: 4f0955fb-8fa3-4102-b2a5-44ce5cbd2e35
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: GetSystemWindowsDirectory, GetSystemWindowsDirectory function, GetSystemWindowsDirectoryA, GetSystemWindowsDirectoryW, _win32_getsystemwindowsdirectory, base.getsystemwindowsdirectory, sysinfoapi/GetSystemWindowsDirectory, sysinfoapi/GetSystemWindowsDirectoryA, sysinfoapi/GetSystemWindowsDirectoryW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetSystemWindowsDirectoryW (Unicode) and GetSystemWindowsDirectoryA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-SysInfo-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-0.dll
 - API-MS-Win-Core-SysInfo-l1-2-1.dll
 - API-MS-Win-Core-SysInfo-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
 - GetSystemWindowsDirectory
 - GetSystemWindowsDirectoryA
 - GetSystemWindowsDirectoryW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetSystemWindowsDirectoryW function


## -description


Retrieves the path of the shared Windows directory on a multi-user system.

This function is provided primarily for compatibility. Applications should store code in the Program Files folder and persistent data in the Application Data folder in the user's profile. For more information, see 
<a href="https://msdn.microsoft.com/a240abc0-e0a6-4f95-8e74-7dc410970212">ShGetFolderPath</a>.


## -parameters




### -param lpBuffer [out]

A pointer to the buffer to receive the path. This path does not end with a backslash unless the Windows directory is the root directory. For example, if the Windows directory is named Windows on drive C, the path of the Windows directory retrieved by this function is C:\Windows. If the system was installed in the root directory of drive C, the path retrieved is C:\.


### -param uSize [in]

The maximum size of the buffer specified by the <i>lpBuffer</i> parameter, in <b>TCHARs</b>.


## -returns



If the function succeeds, the return value is the length of the string copied to the buffer, in <b>TCHARs</b>, not including the terminating null character.

If the length is greater than the size of the buffer, the return value is the size of the buffer required to hold the path.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



On a system that is running Terminal Services, each user has a unique Windows directory. The system Windows directory is shared by all users, so it is the directory where an application should store initialization and help files that apply to all users.

With Terminal Services, the 
<b>GetSystemWindowsDirectory</b> function retrieves the path of the system Windows directory, while the 
<a href="https://msdn.microsoft.com/8c9b55e1-121a-4405-9f83-043752dd48ed">GetWindowsDirectory</a> function retrieves the path of a Windows directory that is private for each user. On a single-user system, 
<b>GetSystemWindowsDirectory</b> is the same as 
<b>GetWindowsDirectory</b>.




## -see-also




<a href="https://msdn.microsoft.com/8c9b55e1-121a-4405-9f83-043752dd48ed">GetWindowsDirectory</a>



<a href="https://msdn.microsoft.com/6fcac066-1ab0-443a-9994-b68ead3bbc20">SHGetFolderLocation</a>



<a href="https://msdn.microsoft.com/aa7deebf-7dce-4147-8a15-1d7411aea0fa">System
		  Information Functions</a>
 

 

