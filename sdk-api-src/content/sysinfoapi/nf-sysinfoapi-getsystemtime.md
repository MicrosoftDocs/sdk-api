---
UID: NF:sysinfoapi.GetSystemTime
title: GetSystemTime function
author: windows-sdk-content
description: Retrieves the current system date and time. The system time is expressed in Coordinated Universal Time (UTC).
old-location: base\getsystemtime.htm
tech.root: sysinfo
ms.assetid: 9ed8386b-f035-446f-b0f8-12e0d3f23aac
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSystemTime, GetSystemTime function, _win32_getsystemtime, base.getsystemtime, sysinfoapi/GetSystemTime
ms.topic: function
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-SysInfo-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-0.dll
 - API-MS-Win-Core-SysInfo-l1-2-1.dll
 - API-MS-Win-Core-SysInfo-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
 - GetSystemTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetSystemTime function


## -description


Retrieves the current system date and time. The system time is expressed in Coordinated Universal Time (UTC).

To retrieve the current system date and time in local time, use the <a href="https://msdn.microsoft.com/a63fcd36-de48-4437-a823-837884cc2bf9">GetLocalTime</a> function.


## -parameters




### -param lpSystemTime [out]

A pointer to a 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure to receive the current system date and time. The <i>lpSystemTime</i> parameter must not be <b>NULL</b>. Using <b>NULL</b> will result in an access violation.


## -returns



This function does not return a value or provide extended error information.




## -remarks



To set the current system date and time, use the <a href="https://msdn.microsoft.com/0768794d-de61-4d5c-96ad-4c4711c72584">SetSystemTime</a> function.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/a63fcd36-de48-4437-a823-837884cc2bf9">GetLocalTime</a>



<a href="https://msdn.microsoft.com/6c748726-c81d-4669-87a1-28aad0fccead">GetSystemTimeAdjustment</a>



<a href="https://msdn.microsoft.com/adf7ff5d-2d30-4490-9868-9ad78ef7a0b6">GetSystemTimeAsFileTime</a>



<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a>



<a href="https://msdn.microsoft.com/0768794d-de61-4d5c-96ad-4c4711c72584">SetSystemTime</a>



<a href="https://msdn.microsoft.com/1a1e251e-2375-4134-bbd8-1e4670b9f9d2">System Time</a>



<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>
 

 

