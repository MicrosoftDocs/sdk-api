---
UID: NF:sysinfoapi.SetLocalTime
title: SetLocalTime function
author: windows-sdk-content
description: Sets the current local time and date.
old-location: base\setlocaltime.htm
tech.root: sysinfo
ms.assetid: c2d2bac7-4171-4b8b-81e8-0e8a1b2794e6
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: SetLocalTime, SetLocalTime function, _win32_setlocaltime, base.setlocaltime, sysinfoapi/SetLocalTime
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
 - API-MS-Win-Core-SysInfo-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-0.dll
 - API-MS-Win-Core-SysInfo-l1-2-1.dll
 - API-MS-Win-Core-SysInfo-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
 - SetLocalTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetLocalTime function


## -description


Sets the current local time and date.


## -parameters




### -param lpSystemTime [in]

A pointer to a 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that contains the new local date and time. 




The <b>wDayOfWeek</b> member of the 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure is ignored.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The calling process must have the SE_SYSTEMTIME_NAME privilege. This privilege is disabled by default. The 
<b>SetLocalTime</b> function enables the SE_SYSTEMTIME_NAME privilege before changing the local time and disables the privilege before returning. For more information, see 
<a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.

The system uses UTC internally. Therefore, when you call 
<b>SetLocalTime</b>, the system uses the current time zone information to perform the conversion, including the daylight saving time setting. Note that the system uses the daylight saving time setting of the current time, not the new time you are setting. Therefore, to ensure the correct result, call 
<b>SetLocalTime</b> a second time, now that the first call has updated the daylight saving time setting.




## -see-also




<a href="https://msdn.microsoft.com/a63fcd36-de48-4437-a823-837884cc2bf9">GetLocalTime</a>



<a href="https://msdn.microsoft.com/9ed8386b-f035-446f-b0f8-12e0d3f23aac">GetSystemTime</a>



<a href="https://msdn.microsoft.com/a6570ec5-ac77-427a-86d9-32cbecc62e37">Local Time</a>



<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a>



<a href="https://msdn.microsoft.com/93c72511-057c-4b26-a4ae-1d225a80c572">SetSystemTimeAdjustment</a>



<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>
 

 

