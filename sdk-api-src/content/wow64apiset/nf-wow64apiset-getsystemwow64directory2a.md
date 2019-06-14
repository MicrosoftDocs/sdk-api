---
UID: NF:wow64apiset.GetSystemWow64Directory2A
title: GetSystemWow64Directory2A function (wow64apiset.h)
author: windows-sdk-content
description: Retrieves the path of the system directory used by WOW64, using the specified image file machine type.
old-location: base\getsystemwow64directory2.htm
tech.root: SysInfo
ms.assetid: 938370BE-6EAB-4198-9AF3-ED8889E1E41F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSystemWow64Directory2, GetSystemWow64Directory2 function, GetSystemWow64Directory2A, GetSystemWow64Directory2W, base.getsystemwow64directory2, wow64apiset/GetSystemWow64Directory2, wow64apiset/GetSystemWow64Directory2A, wow64apiset/GetSystemWow64Directory2W
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
ms.custom: 19H1
---

# GetSystemWow64Directory2A function


## -description


Retrieves the path of the system directory used by <a href="https://docs.microsoft.com/windows/desktop/WinProg64/running-32-bit-applications">WOW64</a>, using the specified image file machine type. This directory is not present on 32-bit Windows.


## -parameters




### -param lpBuffer [out]

A pointer to the buffer to receive the path. This path does not end with a backslash.


### -param uSize [in]

The maximum size of the buffer, in <b>TCHARs</b>.


### -param ImageFileMachineType [in]

An <a href="https://docs.microsoft.com/windows/desktop/SysInfo/image-file-machine-constants">IMAGE_FILE_MACHINE_*</a> value that specifies the machine to test.


## -returns



If the function succeeds, the return value is the length, in <b>TCHARs</b>, of the string copied to the buffer, not including the terminating null character. If the length is greater than the size of the buffer, the return value is the size of the buffer required to hold the path.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



On systems that support multiple <a href="https://docs.microsoft.com/windows/desktop/WinProg64/running-32-bit-applications">WOW64</a> architectures, you can use <b>GetSystemWow64Directory2</b> to retrieve appropriate system directory associated with the WOW64 architecture specified by <i>ImageFileMachineType</i>. 

WOW64 uses the system directory to store shared 32-bit code on 64-bit Windows. Most applications have no need to access this directory explicitly.

For more information on WOW64, see 
<a href="https://docs.microsoft.com/windows/desktop/WinProg64/running-32-bit-applications">Running 32-bit Applications</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directorya">GetSystemWow64Directory</a>
 

 

