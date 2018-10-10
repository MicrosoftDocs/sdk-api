---
UID: NF:timezoneapi.GetDynamicTimeZoneInformation
title: GetDynamicTimeZoneInformation function
author: windows-sdk-content
description: Retrieves the current time zone and dynamic daylight saving time settings. These settings control the translations between Coordinated Universal Time (UTC) and local time.
old-location: base\getdynamictimezoneinformation.htm
tech.root: SysInfo
ms.assetid: 9f96f779-7e4f-4a50-a9dc-f3bc86c76ece
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: GetDynamicTimeZoneInformation, GetDynamicTimeZoneInformation function, base.getdynamictimezoneinformation, timezoneapi/GetDynamicTimeZoneInformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: timezoneapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - GetDynamicTimeZoneInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetDynamicTimeZoneInformation function


## -description


Retrieves the current time zone and dynamic daylight saving time settings. These settings control the translations between Coordinated Universal Time (UTC) and local time.


## -parameters




### -param pTimeZoneInformation [out]

A pointer to a <a href="https://msdn.microsoft.com/d60b1212-26bc-4fad-afce-9bd9062ca5b0">DYNAMIC_TIME_ZONE_INFORMATION</a> structure.


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
Daylight saving time is not used in the current time zone, because there are no transition dates.

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
<a href="https://msdn.microsoft.com/d60b1212-26bc-4fad-afce-9bd9062ca5b0">DYNAMIC_TIME_ZONE_INFORMATION</a> structure. 



							

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
<a href="https://msdn.microsoft.com/d60b1212-26bc-4fad-afce-9bd9062ca5b0">DYNAMIC_TIME_ZONE_INFORMATION</a> structure.

</td>
</tr>
</table>
 

If the function fails, it returns TIME_ZONE_ID_INVALID. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



 The <b>StandardName</b> and <b>DaylightName</b> members  of the resultant <a href="https://msdn.microsoft.com/d60b1212-26bc-4fad-afce-9bd9062ca5b0">DYNAMIC_TIME_ZONE_INFORMATION</a>  structure are localized according to the current user default UI language.




## -see-also




<a href="https://msdn.microsoft.com/d60b1212-26bc-4fad-afce-9bd9062ca5b0">DYNAMIC_TIME_ZONE_INFORMATION</a>



<a href="https://msdn.microsoft.com/98ad7b94-f649-4270-8348-0aba5b59a433">SetDynamicTimeZoneInformation</a>



<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>
 

 

