---
UID: NF:timezoneapi.EnumDynamicTimeZoneInformation
title: EnumDynamicTimeZoneInformation function (timezoneapi.h)
description: Enumerates DYNAMIC_TIME_ZONE_INFORMATION entries stored in the registry.
helpviewer_keywords: ["EnumDynamicTimeZoneInformation","EnumDynamicTimeZoneInformation function","base.enumdynamictimezoneinformation","timezoneapi/EnumDynamicTimeZoneInformation"]
old-location: base\enumdynamictimezoneinformation.htm
tech.root: winprog
ms.assetid: EBB2366A-86FE-4764-B7F9-5D305993CE0A
ms.date: 12/05/2018
ms.keywords: EnumDynamicTimeZoneInformation, EnumDynamicTimeZoneInformation function, base.enumdynamictimezoneinformation, timezoneapi/EnumDynamicTimeZoneInformation
req.header: timezoneapi.h
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
req.lib: advapi32.lib
req.dll: advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EnumDynamicTimeZoneInformation
 - timezoneapi/EnumDynamicTimeZoneInformation
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
 - MinKernelBase.dll
 - advapi32.dll
api_name:
 - EnumDynamicTimeZoneInformation
---

# EnumDynamicTimeZoneInformation function


## -description

Enumerates <a href="/windows/desktop/api/timezoneapi/ns-timezoneapi-dynamic_time_zone_information">DYNAMIC_TIME_ZONE_INFORMATION</a> entries stored in the  registry. This information is used to support time zones that experience annual boundary changes due to daylight saving time adjustments. Use the information returned by this function when calling <a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformationeffectiveyears">GetDynamicTimeZoneInformationEffectiveYears</a> to retrieve the specific range of years to pass to <a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformationforyear">GetTimeZoneInformationForYear</a>.

## -parameters

### -param dwIndex [in]

Index value that represents the location of a <a href="/windows/desktop/api/timezoneapi/ns-timezoneapi-dynamic_time_zone_information">DYNAMIC_TIME_ZONE_INFORMATION</a> entry.

### -param lpTimeZoneInformation [out]

Specifies settings for  a time zone and dynamic daylight saving time.

## -returns

This function returns DWORD. Possible return values include:

| Value                   | Description                                       | 
|-------------------------|---------------------------------------------------|
| ERROR_SUCCESS           | The operation succeeded.                          |
| ERROR_NO_MORE_ITEMS     | No more data is available for the given index.    |
| ERROR_INVALID_PARAMETER | A parameter is invalid.                           |
| Any other value         | The operation failed.                             |

## -remarks

The following example demonstrates looping through the potential timezones until **ERROR_NO_MORE_ITEMS** is returned, indicating that there are no more time zone entries in the registry.

```cpp
std::vector<DYNAMIC_TIME_ZONE_INFORMATION> possibleTimezones;
DYNAMIC_TIME_ZONE_INFORMATION dynamicTimezone = {};
DWORD dwResult = 0;
DWORD i = 0;

do
{
    dwResult = EnumDynamicTimeZoneInformation(i++, &dynamicTimezone);
    if (dwResult == ERROR_SUCCESS)
    {
        possibleTimezones.push_back(dynamicTimezone);
    }
}
while (dwResult != ERROR_NO_MORE_ITEMS);
```

## -see-also

<a href="/windows/desktop/api/timezoneapi/ns-timezoneapi-dynamic_time_zone_information">DYNAMIC_TIME_ZONE_INFORMATION</a>



<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformationeffectiveyears">GetDynamicTimeZoneInformationEffectiveYears</a>
