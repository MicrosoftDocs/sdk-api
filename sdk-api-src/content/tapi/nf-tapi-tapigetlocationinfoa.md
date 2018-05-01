---
UID: NF:tapi.tapiGetLocationInfoA
title: tapiGetLocationInfoA function
author: windows-driver-content
description: The tapiGetLocationInfo function returns the country or region code and city (area) code that the user has set in the current location parameters in the Telephony Control Panel.
old-location: tapi2\tapigetlocationinfo.htm
old-project: Tapi
ms.assetid: c7c83cb7-3fd6-4dbb-8510-2c9afcc7015c
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: "_tapi2_tapigetlocationinfo, tapi/tapiGetLocationInfo, tapi/tapiGetLocationInfoA, tapi/tapiGetLocationInfoW, tapi2.tapigetlocationinfo, tapiGetLocationInfo, tapiGetLocationInfo function [TAPI 2.2], tapiGetLocationInfoA, tapiGetLocationInfoW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: FLICK_POINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Tapi32.dll
api_name:
-	tapiGetLocationInfo
-	tapiGetLocationInfoA
-	tapiGetLocationInfoW
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# tapiGetLocationInfoA function


## -description


The 
<b>tapiGetLocationInfo</b> function returns the country or region code and city (area) code that the user has set in the current location parameters in the Telephony Control Panel. The application can use this information to assist the user in forming proper canonical telephone numbers, such as by offering these as defaults when new numbers are entered in a phone book entry or database record.


## -parameters




### -param lpszCountryCode

Pointer to a memory location where a <b>null</b>-terminated string specifying the country or region code for the current location is to be returned. The application should allocate at least 8 bytes of storage at this location to hold the string (TAPI does not return more than 8 bytes, including the terminating <b>NULL</b>). An empty string (\0) is returned if the country or region code has not been set for the current location.


### -param lpszCityCode

Pointer to a memory location where a <b>null</b>-terminated string specifying the city (area) code for the current location is to be returned. The application should allocate at least 8 bytes of storage at this location to hold the string (TAPI does not return more than 8 bytes, including the terminating <b>NULL</b>). An empty string (\0) is returned if the city code has not been set for the current location.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are TAPIERR_REQUESTFAILED.




## -see-also




<a href="https://msdn.microsoft.com/43ca86b0-0107-4937-b15a-47916e144527">Assisted Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

