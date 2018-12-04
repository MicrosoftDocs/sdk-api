---
UID: NF:wow64apiset.GetSystemWow64DirectoryA
title: GetSystemWow64DirectoryA function
author: windows-sdk-content
description: Retrieves the path of the system directory used by WOW64.
old-location: base\getsystemwow64directory.htm
tech.root: sysinfo
ms.assetid: 31ccd1bf-87c7-4df6-ae9d-5a3dfbd8b38b
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: GetSystemWow64Directory, GetSystemWow64Directory function, GetSystemWow64DirectoryA, GetSystemWow64DirectoryW, _win32_getsystemwow64directory, base.getsystemwow64directory, wow64apiset/GetSystemWow64Directory, wow64apiset/GetSystemWow64DirectoryA, wow64apiset/GetSystemWow64DirectoryW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wow64apiset.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetSystemWow64DirectoryW (Unicode) and GetSystemWow64DirectoryA (ANSI)
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
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-Wow64-l1-1-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetSystemWow64Directory
 - GetSystemWow64DirectoryA
 - GetSystemWow64DirectoryW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetSystemWow64DirectoryA function


## -description


Retrieves the path of the system directory used by WOW64. This directory is not present on 32-bit Windows.


## -parameters




### -param lpBuffer [out]

A pointer to the buffer to receive the path. This path does not end with a backslash.


### -param uSize [in]

The maximum size of the buffer, in <b>TCHARs</b>.


## -returns



If the function succeeds, the return value is the length, in <b>TCHARs</b>, of the string copied to the buffer, not including the terminating null character. If the length is greater than the size of the buffer, the return value is the size of the buffer required to hold the path.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

On 32-bit Windows, the function always fails, and the extended error is set to ERROR_CALL_NOT_IMPLEMENTED.




## -remarks



WOW64 uses the system directory to store shared 32-bit code on 64-bit Windows. Most applications have no need to access this directory explicitly.

For more information on WOW64, see 
<a href="https://msdn.microsoft.com/ac75c5af-86e8-4282-9a8e-8db3c22cbda0">Running 32-bit Applications</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0501 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/aa7deebf-7dce-4147-8a15-1d7411aea0fa">System
    Information Functions</a>
 

 

