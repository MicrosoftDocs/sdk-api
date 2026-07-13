---
UID: NF:tapi.lineGetCountryA
title: lineGetCountryA function (tapi.h)
description: The lineGetCountry function fetches the stored dialing rules and other information related to a specified country/region, the first country/region in the country/region list, or all countries/regions. (lineGetCountryA)
helpviewer_keywords: ["lineGetCountryA", "tapi/lineGetCountryA"]
old-location: tapi2\linegetcountry.htm
tech.root: tapi3
ms.assetid: 4de271b3-d93b-4fc9-b853-e26ef1ae75ae
ms.date: 12/05/2018
ms.keywords: _tapi2_linegetcountry, lineGetCountry, lineGetCountry function [TAPI 2.2], lineGetCountryA, lineGetCountryW, tapi/lineGetCountry, tapi/lineGetCountryA, tapi/lineGetCountryW, tapi2.linegetcountry
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineGetCountryW (Unicode) and lineGetCountryA (ANSI)
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
 - lineGetCountryA
 - tapi/lineGetCountryA
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
 - lineGetCountry
 - lineGetCountryA
 - lineGetCountryW
---

# lineGetCountryA function


## -description

The 
<b>lineGetCountry</b> function fetches the stored dialing rules and other information related to a specified country/region, the first country/region in the country/region list, or all countries/regions.

## -parameters

### -param dwCountryID

Country/region identifier (not the country code) of the country/region for which information is to be obtained. If the value 1 is specified, information on the first country/region in the country/region list is obtained. If the value 0 is specified, information on all countries/regions is obtained (which can require a great deal of memory — 20 KB or more).

### -param dwAPIVersion

Highest version of TAPI supported by the application (not necessarily the value negotiated by 
<a href="/windows/desktop/api/tapi/nf-tapi-linenegotiateapiversion">lineNegotiateAPIVersion</a> on some particular line device).

### -param lpLineCountryList

Pointer to a location to which a <a href="/windows/desktop/api/tapi/ns-tapi-linecountrylist">LINECOUNTRYLIST</a> structure is loaded. Prior to calling 
<b>lineGetCountry</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="/windows/desktop/Tapi/memory-allocation">memory allocation</a> topic.</div>
<div> </div>

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_NOMEM, LINEERR_INIFILECORRUPT, LINEERR_OPERATIONFAILED, LINEERR_INVALCOUNTRYCODE, LINEERR_STRUCTURETOOSMALL, LINEERR_INVALPOINTER.

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecountrylist">LINECOUNTRYLIST</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linenegotiateapiversion">lineNegotiateAPIVersion</a>

## -remarks

> [!NOTE]
> The tapi.h header defines lineGetCountry as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
