---
UID: NF:sysinfoapi.GetSystemDirectoryA
title: GetSystemDirectoryA function
author: windows-sdk-content
description: Retrieves the path of the system directory.
old-location: base\getsystemdirectory.htm
tech.root: sysinfo
ms.assetid: 79f045b2-40d9-498a-b720-e729c92bf50b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSystemDirectory, GetSystemDirectory function, GetSystemDirectoryA, GetSystemDirectoryW, _win32_getsystemdirectory, base.getsystemdirectory, sysinfoapi/GetSystemDirectory, sysinfoapi/GetSystemDirectoryA, sysinfoapi/GetSystemDirectoryW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetSystemDirectoryW (Unicode) and GetSystemDirectoryA (ANSI)
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
 - GetSystemDirectory
 - GetSystemDirectoryA
 - GetSystemDirectoryW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetSystemDirectoryA function


## -description


Retrieves the path of the system directory. The system directory contains system files such as dynamic-link libraries and drivers.

This function is provided primarily for compatibility. Applications should store code in the Program Files folder and persistent data in the Application Data folder in the user's profile. For more information, see 
<a href="https://msdn.microsoft.com/a240abc0-e0a6-4f95-8e74-7dc410970212">ShGetFolderPath</a>.


## -parameters




### -param lpBuffer [out]

A pointer to the buffer to receive the path. This path does not end with a backslash unless the system directory is the root directory. For example, if the system directory is named Windows\System32 on drive C, the path of the system directory retrieved by this function is C:\Windows\System32.


### -param uSize [in]

The maximum size of the buffer, in <b>TCHARs</b>.


## -returns



If the function succeeds, the return value is the length, in <b>TCHARs</b>, of the string copied to the buffer, not including the terminating null character. If the length is greater than the size of the buffer, the return value is the size of the buffer required to hold the path, including the terminating null character.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Applications should not create files in the system directory. If the user is running a shared version of the operating system, the application does not have write access to the system directory.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/965bd14b-be93-4084-bce8-642f5704cef1">Getting System Information</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1fbe6289-2ca8-4ca8-b004-ecf513f9b0bd">GetCurrentDirectory</a>



<a href="https://msdn.microsoft.com/8c9b55e1-121a-4405-9f83-043752dd48ed">GetWindowsDirectory</a>



<a href="https://msdn.microsoft.com/02dd0a2b-8072-4ce5-99b4-ffa6dcbd46cd">SetCurrentDirectory</a>



<a href="https://msdn.microsoft.com/aa7deebf-7dce-4147-8a15-1d7411aea0fa">System
		  Information Functions</a>
 

 

