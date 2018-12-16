---
UID: NF:timezoneapi.TzSpecificLocalTimeToSystemTime
title: TzSpecificLocalTimeToSystemTime function
author: windows-sdk-content
description: Converts a local time to a time in Coordinated Universal Time (UTC).
old-location: base\tzspecificlocaltimetosystemtime.htm
tech.root: sysinfo
ms.assetid: d671499a-027d-4b1f-ae16-8b1978eb9783
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TzSpecificLocalTimeToSystemTime, TzSpecificLocalTimeToSystemTime function, _win32_tzspecificlocaltimetosystemtime, base.tzspecificlocaltimetosystemtime, timezoneapi/TzSpecificLocalTimeToSystemTime
ms.topic: function
req.header: timezoneapi.h
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
 - API-MS-Win-Core-SysInfo-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-TimeZone-l1-1-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - TzSpecificLocalTimeToSystemTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TzSpecificLocalTimeToSystemTime function


## -description


Converts a local time to a time in Coordinated Universal Time (UTC).


## -parameters




### -param lpTimeZoneInformation [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/18c10ad6-8bc9-4a3b-a424-d17ee1d9e004">TIME_ZONE_INFORMATION</a> structure that specifies the time zone for the time specified in <i>lpLocalTime</i>.

If <i>lpTimeZoneInformation</i> is <b>NULL</b>, the function uses the currently active time zone.


### -param lpLocalTime [in]

A pointer to a 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that specifies the local time to be converted. The function converts this time to the corresponding UTC time.


### -param lpUniversalTime [out]

A pointer to a 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that receives the UTC time.


## -returns



If the function succeeds, the return value is nonzero, and the function sets the members of the 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure pointed to by <i>lpUniversalTime</i> to the appropriate values.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>TzSpecificLocalTimeToSystemTime</b> takes into account whether daylight saving time (DST) is in effect for the local time to be converted.




## -see-also




<a href="https://msdn.microsoft.com/9ed8386b-f035-446f-b0f8-12e0d3f23aac">GetSystemTime</a>



<a href="https://msdn.microsoft.com/3d7601a5-6d22-4b1a-a222-9db46d21a3c7">GetTimeZoneInformation</a>



<a href="https://msdn.microsoft.com/a6570ec5-ac77-427a-86d9-32cbecc62e37">Local Time</a>



<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a>



<a href="https://msdn.microsoft.com/f3a87ec2-67a0-418f-af6e-6c0b5547cffb">SystemTimeToTzSpecificLocalTime</a>



<a href="https://msdn.microsoft.com/18c10ad6-8bc9-4a3b-a424-d17ee1d9e004">TIME_ZONE_INFORMATION</a>



<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>
 

 

