---
UID: NF:sysinfoapi.GetSystemTimeAsFileTime
title: GetSystemTimeAsFileTime function
author: windows-sdk-content
description: Retrieves the current system date and time. The information is in Coordinated Universal Time (UTC) format.
old-location: base\getsystemtimeasfiletime.htm
tech.root: sysinfo
ms.assetid: adf7ff5d-2d30-4490-9868-9ad78ef7a0b6
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: GetSystemTimeAsFileTime, GetSystemTimeAsFileTime function, _win32_getsystemtimeasfiletime, base.getsystemtimeasfiletime, sysinfoapi/GetSystemTimeAsFileTime
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
 - GetSystemTimeAsFileTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetSystemTimeAsFileTime function


## -description


Retrieves the current system date and time. The information is in Coordinated Universal Time (UTC) format.


## -parameters




### -param lpSystemTimeAsFileTime [out]

A pointer to a 
<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure to receive the current system date and time in UTC format.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/52d80b82-9ab0-4631-9e70-85df21da4946">File Times</a>



<a href="https://msdn.microsoft.com/9ed8386b-f035-446f-b0f8-12e0d3f23aac">GetSystemTime</a>



<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a>



<a href="https://msdn.microsoft.com/1a1e251e-2375-4134-bbd8-1e4670b9f9d2">System Time</a>



<a href="https://msdn.microsoft.com/d19594bc-8238-4a8f-882d-5b9019ef4880">SystemTimeToFileTime</a>



<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>
 

 

