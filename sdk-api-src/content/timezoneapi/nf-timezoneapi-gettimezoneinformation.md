---
UID: NF:timezoneapi.GetTimeZoneInformation
title: GetTimeZoneInformation function
author: windows-sdk-content
description: Retrieves the current time zone settings. These settings control the translations between Coordinated Universal Time (UTC) and local time.
old-location: base\gettimezoneinformation.htm
tech.root: SysInfo
ms.assetid: 3d7601a5-6d22-4b1a-a222-9db46d21a3c7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetTimeZoneInformation, GetTimeZoneInformation function, _win32_gettimezoneinformation, base.gettimezoneinformation, timezoneapi/GetTimeZoneInformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: timezoneapi.h
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
 - API-MS-Win-Core-TimeZone-l1-1-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - GetTimeZoneInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetTimeZoneInformation function


## -description


Retrieves the current time zone settings. These settings control the translations between Coordinated Universal Time (UTC) and local time.

To support boundaries for daylight saving time that change from year to year, use the <a href="https://msdn.microsoft.com/9f96f779-7e4f-4a50-a9dc-f3bc86c76ece">GetDynamicTimeZoneInformation</a>  or <a href="https://msdn.microsoft.com/5bd29a25-98f0-439e-be88-8011bbf98926">GetTimeZoneInformationForYear</a> function.


## -parameters




### -param lpTimeZoneInformation [out]

A pointer to a 
<a href="https://msdn.microsoft.com/18c10ad6-8bc9-4a3b-a424-d17ee1d9e004">TIME_ZONE_INFORMATION</a> structure to receive the current settings.


## -returns



If the function succeeds, it returns one of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TIME_ZONE_ID_UNKNOWN</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Daylight saving time is not used in the current time zone, because there are no transition dates or automatic adjustment for daylight saving time is disabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TIME_ZONE_ID_STANDARD</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The system is operating in the range covered by the <b>StandardDate</b> member of the 
<a href="https://msdn.microsoft.com/18c10ad6-8bc9-4a3b-a424-d17ee1d9e004">TIME_ZONE_INFORMATION</a> structure. 



							

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TIME_ZONE_ID_DAYLIGHT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The system is operating in the range covered by the <b>DaylightDate</b> member of the 
<a href="https://msdn.microsoft.com/18c10ad6-8bc9-4a3b-a424-d17ee1d9e004">TIME_ZONE_INFORMATION</a> structure.

</td>
</tr>
</table>
 

If the function fails for other reasons, such as an out of memory error, it returns TIME_ZONE_ID_INVALID. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All translations between UTC time and local time are based on the following formula:

UTC = local time + bias

The bias is the difference, in minutes, between UTC time and local time.

 The <b>StandardName</b> and <b>DaylightName</b> members  of the resultant <a href="https://msdn.microsoft.com/18c10ad6-8bc9-4a3b-a424-d17ee1d9e004">TIME_ZONE_INFORMATION</a>  structure are localized according to the current user default UI language.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/afb13501-3a87-433a-a05e-139103060109">SetTimeZoneInformation</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9f96f779-7e4f-4a50-a9dc-f3bc86c76ece">GetDynamicTimeZoneInformation</a>



<a href="https://msdn.microsoft.com/5bd29a25-98f0-439e-be88-8011bbf98926">GetTimeZoneInformationForYear</a>



<a href="https://msdn.microsoft.com/a6570ec5-ac77-427a-86d9-32cbecc62e37">Local Time</a>



<a href="https://msdn.microsoft.com/afb13501-3a87-433a-a05e-139103060109">SetTimeZoneInformation</a>



<a href="https://msdn.microsoft.com/18c10ad6-8bc9-4a3b-a424-d17ee1d9e004">TIME_ZONE_INFORMATION</a>



<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>
 

 

