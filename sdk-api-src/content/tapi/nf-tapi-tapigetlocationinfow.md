---
UID: NF:tapi.tapiGetLocationInfoW
title: tapiGetLocationInfoW function (tapi.h)
description: The tapiGetLocationInfoW (Unicode) function (tapi.h) returns the country, region, and city code that the user has set in the location parameters in the Telephony Control Panel. 
helpviewer_keywords: ["_tapi2_tapigetlocationinfo", "tapi/tapiGetLocationInfo", "tapi/tapiGetLocationInfoW", "tapi2.tapigetlocationinfo", "tapiGetLocationInfo", "tapiGetLocationInfo function [TAPI 2.2]", "tapiGetLocationInfoW"]
old-location: tapi2\tapigetlocationinfo.htm
tech.root: tapi3
ms.assetid: c7c83cb7-3fd6-4dbb-8510-2c9afcc7015c
ms.date: 08/09/2022
ms.keywords: _tapi2_tapigetlocationinfo, tapi/tapiGetLocationInfo, tapi/tapiGetLocationInfoA, tapi/tapiGetLocationInfoW, tapi2.tapigetlocationinfo, tapiGetLocationInfo, tapiGetLocationInfo function [TAPI 2.2], tapiGetLocationInfoA, tapiGetLocationInfoW
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: tapiGetLocationInfoW (Unicode) and tapiGetLocationInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tapiGetLocationInfoW
 - tapi/tapiGetLocationInfoW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - tapiGetLocationInfo
 - tapiGetLocationInfoA
 - tapiGetLocationInfoW
---

# tapiGetLocationInfoW function


## -description

The 
<b>tapiGetLocationInfo</b> function returns the country or region code and city (area) code that the user has set in the current location parameters in the Telephony Control Panel. The application can use this information to assist the user in forming proper canonical telephone numbers, such as by offering these as defaults when new numbers are entered in a phone book entry or database record.

## -parameters

### -param lpszCountryCodeW

Pointer to a memory location where a <b>null</b>-terminated string specifying the country or region code for the current location is to be returned. The application should allocate at least 8 bytes of storage at this location to hold the string (TAPI does not return more than 8 bytes, including the terminating <b>NULL</b>). An empty string (\0) is returned if the country or region code has not been set for the current location.

### -param lpszCityCodeW

Pointer to a memory location where a <b>null</b>-terminated string specifying the city (area) code for the current location is to be returned. The application should allocate at least 8 bytes of storage at this location to hold the string (TAPI does not return more than 8 bytes, including the terminating <b>NULL</b>). An empty string (\0) is returned if the city code has not been set for the current location.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are TAPIERR_REQUESTFAILED.

## -see-also

<a href="/windows/desktop/Tapi/assisted-telephony-services-reference">Assisted Telephony Services Reference</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>

## -remarks

> [!NOTE]
> The tapi.h header defines tapiGetLocationInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
