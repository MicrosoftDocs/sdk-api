---
UID: NF:timezoneapi.SetDynamicTimeZoneInformation
title: SetDynamicTimeZoneInformation function
author: windows-sdk-content
description: Sets the current time zone and dynamic daylight saving time settings. These settings control translations from Coordinated Universal Time (UTC) to local time.
old-location: base\setdynamictimezoneinformation.htm
tech.root: sysinfo
ms.assetid: 98ad7b94-f649-4270-8348-0aba5b59a433
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: SetDynamicTimeZoneInformation, SetDynamicTimeZoneInformation function, base.setdynamictimezoneinformation, timezoneapi/SetDynamicTimeZoneInformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: timezoneapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - API-MS-Win-Core-TimeZone-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - SetDynamicTimeZoneInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetDynamicTimeZoneInformation function


## -description


Sets the current time zone and dynamic daylight saving time settings. These settings control translations from Coordinated Universal Time (UTC) to local time.


## -parameters




### -param lpTimeZoneInformation [in]

A pointer to a <a href="https://msdn.microsoft.com/d60b1212-26bc-4fad-afce-9bd9062ca5b0">DYNAMIC_TIME_ZONE_INFORMATION</a> structure.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



An application must have the SE_TIME_ZONE_NAME privilege for this function to succeed. This privilege is disabled by default. Use the 
<a href="https://msdn.microsoft.com/8e3f70cd-814e-4aab-8f48-0ca482beef2e">AdjustTokenPrivileges</a> function to enable the privilege before calling 
<b>SetDynamicTimeZoneInformation</b>, and then to disable the privilege after the 
<b>SetDynamicTimeZoneInformation</b> call. For more information, see 
<a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.




## -see-also




<a href="https://msdn.microsoft.com/d60b1212-26bc-4fad-afce-9bd9062ca5b0">DYNAMIC_TIME_ZONE_INFORMATION</a>



<a href="https://msdn.microsoft.com/9f96f779-7e4f-4a50-a9dc-f3bc86c76ece">GetDynamicTimeZoneInformation</a>



<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>
 

 

