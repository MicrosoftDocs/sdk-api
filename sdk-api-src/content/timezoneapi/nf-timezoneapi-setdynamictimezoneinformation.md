---
UID: NF:timezoneapi.SetDynamicTimeZoneInformation
title: SetDynamicTimeZoneInformation function (timezoneapi.h)
description: Sets the current time zone and dynamic daylight saving time settings. These settings control translations from Coordinated Universal Time (UTC) to local time.
helpviewer_keywords: ["SetDynamicTimeZoneInformation","SetDynamicTimeZoneInformation function","base.setdynamictimezoneinformation","timezoneapi/SetDynamicTimeZoneInformation"]
old-location: base\setdynamictimezoneinformation.htm
tech.root: winprog
ms.assetid: 98ad7b94-f649-4270-8348-0aba5b59a433
ms.date: 12/05/2018
ms.keywords: SetDynamicTimeZoneInformation, SetDynamicTimeZoneInformation function, base.setdynamictimezoneinformation, timezoneapi/SetDynamicTimeZoneInformation
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetDynamicTimeZoneInformation
 - timezoneapi/SetDynamicTimeZoneInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-timezone-l1-1-1.dll
 - Kernel32.dll
 - API-MS-Win-Core-TimeZone-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - SetDynamicTimeZoneInformation
---

# SetDynamicTimeZoneInformation function


## -description

Sets the current time zone and dynamic daylight saving time settings. These settings control translations from Coordinated Universal Time (UTC) to local time.

## -parameters

### -param lpTimeZoneInformation [in]

A pointer to a <a href="/windows/desktop/api/timezoneapi/ns-timezoneapi-dynamic_time_zone_information">DYNAMIC_TIME_ZONE_INFORMATION</a> structure.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

An application must have the SE_TIME_ZONE_NAME privilege for this function to succeed. This privilege is disabled by default. Use the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges">AdjustTokenPrivileges</a> function to enable the privilege before calling 
<b>SetDynamicTimeZoneInformation</b>, and then to disable the privilege after the 
<b>SetDynamicTimeZoneInformation</b> call. For more information, see 
<a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.

## -see-also

<a href="/windows/desktop/api/timezoneapi/ns-timezoneapi-dynamic_time_zone_information">DYNAMIC_TIME_ZONE_INFORMATION</a>



<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformation">GetDynamicTimeZoneInformation</a>



<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>