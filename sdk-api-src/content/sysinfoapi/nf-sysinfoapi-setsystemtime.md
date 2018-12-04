---
UID: NF:sysinfoapi.SetSystemTime
title: SetSystemTime function
author: windows-sdk-content
description: Sets the current system time and date. The system time is expressed in Coordinated Universal Time (UTC).
old-location: base\setsystemtime.htm
tech.root: sysinfo
ms.assetid: 0768794d-de61-4d5c-96ad-4c4711c72584
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: SetSystemTime, SetSystemTime function, _win32_setsystemtime, base.setsystemtime, sysinfoapi/SetSystemTime
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
 - SetSystemTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetSystemTime function


## -description


Sets the current system time and date. The system time is expressed in Coordinated Universal Time (UTC).


## -parameters




### -param lpSystemTime [in]

A pointer to a 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that contains the new system date and time. 




The <b>wDayOfWeek</b> member of the 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure is ignored.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The calling process must have the SE_SYSTEMTIME_NAME privilege. This privilege is disabled by default. The 
<b>SetSystemTime</b> function enables the SE_SYSTEMTIME_NAME privilege before changing the system time and disables the privilege before returning. For more information, see 
<a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.




## -see-also




<a href="https://msdn.microsoft.com/9ed8386b-f035-446f-b0f8-12e0d3f23aac">GetSystemTime</a>



<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a>



<a href="https://msdn.microsoft.com/93c72511-057c-4b26-a4ae-1d225a80c572">SetSystemTimeAdjustment</a>



<a href="https://msdn.microsoft.com/1a1e251e-2375-4134-bbd8-1e4670b9f9d2">System Time</a>



<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>
 

 

