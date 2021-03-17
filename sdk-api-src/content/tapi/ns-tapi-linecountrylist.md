---
UID: NS:tapi.linecountrylist_tag
title: LINECOUNTRYLIST (tapi.h)
description: The LINECOUNTRYLIST structure describes a list of countries/regions. This structure can contain an array of LINECOUNTRYENTRY structures. LINECOUNTRYLIST is returned by the lineGetCountry function.
helpviewer_keywords: ["*LPLINECOUNTRYLIST","LINECOUNTRYLIST","LINECOUNTRYLIST structure [TAPI 2.2]","LPLINECOUNTRYLIST","LPLINECOUNTRYLIST structure pointer [TAPI 2.2]","_tapi2_linecountrylist_str","tapi/LINECOUNTRYLIST","tapi/LPLINECOUNTRYLIST","tapi2.linecountrylist_str"]
old-location: tapi2\linecountrylist_str.htm
tech.root: tapi3
ms.assetid: f6634d40-0c17-4eb1-a0ca-9590e9e649e2
ms.date: 12/05/2018
ms.keywords: '*LPLINECOUNTRYLIST, LINECOUNTRYLIST, LINECOUNTRYLIST structure [TAPI 2.2], LPLINECOUNTRYLIST, LPLINECOUNTRYLIST structure pointer [TAPI 2.2], _tapi2_linecountrylist_str, tapi/LINECOUNTRYLIST, tapi/LPLINECOUNTRYLIST, tapi2.linecountrylist_str'
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LINECOUNTRYLIST, *LPLINECOUNTRYLIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - linecountrylist_tag
 - tapi/linecountrylist_tag
 - LPLINECOUNTRYLIST
 - tapi/LPLINECOUNTRYLIST
 - LINECOUNTRYLIST
 - tapi/LINECOUNTRYLIST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINECOUNTRYLIST
---

# LINECOUNTRYLIST structure


## -description

The 
<b>LINECOUNTRYLIST</b> structure describes a list of countries/regions. This structure can contain an array of 
<a href="/windows/desktop/api/tapi/ns-tapi-linecountryentry">LINECOUNTRYENTRY</a> structures. 
<b>LINECOUNTRYLIST</b> is returned by the 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetcountry">lineGetCountry</a> function.

## -struct-fields

### -field dwTotalSize

Total size allocated to this data structure, in bytes.

### -field dwNeededSize

Size for this data structure that is needed to hold all the returned information, in bytes.

### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.

### -field dwNumCountries

Number of 
<a href="/windows/desktop/api/tapi/ns-tapi-linecountryentry">LINECOUNTRYENTRY</a> structures present in the array defined by <b>dwCountryListSize</b> and <b>dwCountryListOffset</b>.

### -field dwCountryListSize

Size of the array of country/region information, in bytes.

### -field dwCountryListOffset

Offset from the beginning of the structure to an array of 
<a href="/windows/desktop/api/tapi/ns-tapi-linecountryentry">LINECOUNTRYENTRY</a> structures that provides the information for each country/region. The size of the field is specified by <b>dwCountryListSize</b>.

## -remarks

This structure may not be extended.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linecountryentry">LINECOUNTRYENTRY</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetcountry">lineGetCountry</a>