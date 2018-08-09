---
UID: NF:processthreadsapi.GetProcessVersion
title: GetProcessVersion function
author: windows-sdk-content
description: Retrieves the major and minor version numbers of the system on which the specified process expects to run.
old-location: base\getprocessversion.htm
old-project: procthread
ms.assetid: ed12f2e5-1674-4885-878f-9ba39415780c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetProcessVersion, GetProcessVersion function, _win32_getprocessversion, base.getprocessversion, processthreadsapi/GetProcessVersion, winbase/GetProcessVersion
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PSS_VA_SPACE_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetProcessVersion
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: ADAM
---

# GetProcessVersion function


## -description


Retrieves the major and minor version numbers of the system on which the specified process expects to run.


## -parameters




### -param ProcessId [in]

The process identifier of the process of interest. A value of zero specifies the calling process.


## -returns



If the function succeeds, the return value is the version of the system on which the process expects to run. The high word of the return value contains the major version number. The low word of the return value contains the minor version number.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The function fails if <i>ProcessId</i> is an invalid value.




## -remarks



The 
<b>GetProcessVersion</b> function performs less quickly when <i>ProcessId</i> is nonzero, specifying a process other than the calling process.

The version number returned by this function is the version number stamped in the image header of the .exe file the process is running. Linker programs set this value.

If this function is called from a 32-bit application running on WOW64, the specified process must be a 32-bit process or the function fails.




## -see-also




<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/4bdec0f5-7276-422e-9935-0e231b0fc17d">Processes</a>
 

 

