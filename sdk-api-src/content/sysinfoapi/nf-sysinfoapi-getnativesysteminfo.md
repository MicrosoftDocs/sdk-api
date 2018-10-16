---
UID: NF:sysinfoapi.GetNativeSystemInfo
title: GetNativeSystemInfo function
author: windows-sdk-content
description: Retrieves information about the current system to an application running under WOW64.
old-location: base\getnativesysteminfo.htm
tech.root: sysinfo
ms.assetid: a4a1123b-83d7-4ee2-aa38-68fff5373618
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetNativeSystemInfo, GetNativeSystemInfo function, _win32_getnativesysteminfo, base.getnativesysteminfo, sysinfoapi/GetNativeSystemInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - API-MS-Win-Core-SysInfo-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-1.dll
 - API-MS-Win-Core-SysInfo-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
 - GetNativeSystemInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetNativeSystemInfo function


## -description


Retrieves information about the current system to an application running under 
<a href="https://msdn.microsoft.com/ac75c5af-86e8-4282-9a8e-8db3c22cbda0">WOW64</a>. If the function is called from a 64-bit application, or on a 64-bit system that does not have an Intel64 or x64 processor (such as ARM64), it is equivalent to the 
<a href="https://msdn.microsoft.com/f6d745af-729a-494e-90b4-19fe7d97c7af">GetSystemInfo</a> function.


## -parameters




### -param lpSystemInfo [out]

A pointer to a 
<a href="https://msdn.microsoft.com/971293b8-0af0-4bdf-a7d7-6b1bb80a469c">SYSTEM_INFO</a> structure that receives the information.


## -returns



This function does not return a value.




## -remarks



To determine whether a Win32-based application is running under WOW64, call the 
<a href="https://msdn.microsoft.com/77B4E3C8-F9DE-4674-9CEA-9C81AEEB393C">IsWow64Process2</a> function.

To compile an application that uses this function, define _WIN32_WINNT as 0x0501 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/ae851aef-27d5-4eb7-aeb2-ccdfbf040e5a">Getting the System Version</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/5a237542-e432-487c-aa59-2ede427dd1eb">IsWow64Process</a>



<a href="https://msdn.microsoft.com/971293b8-0af0-4bdf-a7d7-6b1bb80a469c">SYSTEM_INFO</a>



<a href="https://msdn.microsoft.com/aa7deebf-7dce-4147-8a15-1d7411aea0fa">System
		  Information Functions</a>
 

 

