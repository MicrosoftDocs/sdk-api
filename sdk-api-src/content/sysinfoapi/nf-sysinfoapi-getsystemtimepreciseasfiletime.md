---
UID: NF:sysinfoapi.GetSystemTimePreciseAsFileTime
title: GetSystemTimePreciseAsFileTime function
author: windows-sdk-content
description: GetSystemTimePreciseAsFileTime function retrieves the current system date and time with the highest possible level of precision (&lt;1us). The retrieved information is in Coordinated Universal Time (UTC) format.
old-location: base\getsystemtimepreciseasfiletime.htm
tech.root: sysinfo
ms.assetid: 8949C2D4-AE5A-4E18-9B06-F2F13EFA8A5E
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: GetSystemTimePreciseAsFileTime, GetSystemTimePreciseAsFileTime function, base.getsystemtimepreciseasfiletime, sysinfoapi/GetSystemTimePreciseAsFileTime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
 - GetSystemTimePreciseAsFileTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetSystemTimePreciseAsFileTime function


## -description


The 
    <b>GetSystemTimePreciseAsFileTime</b> 
    function retrieves the current system date and time with the highest possible level of precision (&lt;1us). The 
    retrieved information is in Coordinated Universal Time (UTC) format.


## -parameters




### -param lpSystemTimeAsFileTime [out]

Type: <b>LPFILETIME</b>

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the 
      current system date and time in UTC format.


## -returns



This function doesn't return a value.




## -remarks



<div class="alert"><b>Note</b>  This function is best suited for high-resolution time-of-day measurements, or time stamps that are synchronized to UTC. For high-resolution interval measurements, use <a href="https://msdn.microsoft.com/08169390-940b-4110-813a-249d107cc953">QueryPerformanceCounter</a> or <a href="https://msdn.microsoft.com/ee1dbd20-5502-4448-b39a-4629ddc73d01">KeQueryPerformanceCounter</a>. For more info about acquiring high-resolution time stamps, see <a href="https://msdn.microsoft.com/D66E0FC2-3AF2-489B-B4B5-78648905B77B">Acquiring high-resolution time stamps</a>.</div>
<div> </div>


