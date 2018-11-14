---
UID: NF:wow64apiset.GetSystemWow64Directory2A
title: GetSystemWow64Directory2A function
author: windows-sdk-content
description: Retrieves the path of the system directory used by WOW64, using the specified image file machine type.
old-location: base\getsystemwow64directory2.htm
tech.root: sysinfo
ms.assetid: 938370BE-6EAB-4198-9AF3-ED8889E1E41F
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: GetSystemWow64Directory2, GetSystemWow64Directory2 function, GetSystemWow64Directory2A, GetSystemWow64Directory2W, base.getsystemwow64directory2, wow64apiset/GetSystemWow64Directory2, wow64apiset/GetSystemWow64Directory2A, wow64apiset/GetSystemWow64Directory2W
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wow64apiset.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1511 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetSystemWow64Directory2W (Unicode) and GetSystemWow64Directory2A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.dll
req.dll: Kernel32.lib
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.lib
 - API-MS-Win-Core-Wow64-L1-1-1.dll
 - KernelBase.dll
api_name:
 - GetSystemWow64Directory2
 - GetSystemWow64Directory2A
 - GetSystemWow64Directory2W
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetSystemWow64Directory2A
: 
---

# GetSystemWow64Directory2A function


## -description


Retrieves the path of the system directory used by <a href="https://msdn.microsoft.com/ac75c5af-86e8-4282-9a8e-8db3c22cbda0">WOW64</a>, using the specified image file machine type. This directory is not present on 32-bit Windows.


## -parameters




### -param lpBuffer [out]

A pointer to the buffer to receive the path. This path does not end with a backslash.


### -param uSize [in]

The maximum size of the buffer, in <b>TCHARs</b>.


### -param ImageFileMachineType [in]

An <a href="https://msdn.microsoft.com/1E5E4F98-925B-424D-9B3D-BC6716FBF990">IMAGE_FILE_MACHINE_*</a> value that specifies the machine to test.


## -returns



If the function succeeds, the return value is the length, in <b>TCHARs</b>, of the string copied to the buffer, not including the terminating null character. If the length is greater than the size of the buffer, the return value is the size of the buffer required to hold the path.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



On systems that support multiple <a href="https://msdn.microsoft.com/ac75c5af-86e8-4282-9a8e-8db3c22cbda0">WOW64</a> architectures, you can use <b>GetSystemWow64Directory2</b> to retrieve appropriate system directory associated with the WOW64 architecture specified by <i>ImageFileMachineType</i>. 

WOW64 uses the system directory to store shared 32-bit code on 64-bit Windows. Most applications have no need to access this directory explicitly.

For more information on WOW64, see 
<a href="https://msdn.microsoft.com/ac75c5af-86e8-4282-9a8e-8db3c22cbda0">Running 32-bit Applications</a>.




## -see-also




<a href="https://msdn.microsoft.com/31ccd1bf-87c7-4df6-ae9d-5a3dfbd8b38b">GetSystemWow64Directory</a>
 

 

