---
UID: NS:tapi.linetranslatecaps_tag
title: LINETRANSLATECAPS (tapi.h)
description: The LINETRANSLATECAPS structure describes the address translation capabilities.
helpviewer_keywords: ["*LPLINETRANSLATECAPS","LINETRANSLATECAPS","LINETRANSLATECAPS structure [TAPI 2.2]","LPLINETRANSLATECAPS","LPLINETRANSLATECAPS structure pointer [TAPI 2.2]","_tapi2_linetranslatecaps_str","tapi/LINETRANSLATECAPS","tapi/LPLINETRANSLATECAPS","tapi2.linetranslatecaps_str"]
old-location: tapi2\linetranslatecaps_str.htm
tech.root: tapi3
ms.assetid: 9b4dcbe6-41e9-4b9c-9150-d0c7edef5a19
ms.date: 12/05/2018
ms.keywords: '*LPLINETRANSLATECAPS, LINETRANSLATECAPS, LINETRANSLATECAPS structure [TAPI 2.2], LPLINETRANSLATECAPS, LPLINETRANSLATECAPS structure pointer [TAPI 2.2], _tapi2_linetranslatecaps_str, tapi/LINETRANSLATECAPS, tapi/LPLINETRANSLATECAPS, tapi2.linetranslatecaps_str'
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
req.typenames: LINETRANSLATECAPS, *LPLINETRANSLATECAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - linetranslatecaps_tag
 - tapi/linetranslatecaps_tag
 - LPLINETRANSLATECAPS
 - tapi/LPLINETRANSLATECAPS
 - LINETRANSLATECAPS
 - tapi/LINETRANSLATECAPS
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
 - LINETRANSLATECAPS
---

# LINETRANSLATECAPS structure


## -description

The 
<b>LINETRANSLATECAPS</b> structure describes the address translation capabilities. This structure can contain an array of 
<a href="/windows/desktop/api/tapi/ns-tapi-linelocationentry">LINELOCATIONENTRY</a> structures and an array of 
<a href="/windows/desktop/api/tapi/ns-tapi-linecardentry">LINECARDENTRY</a> structures. The 
<b>LINETRANSLATECAPS</b> structure is returned by the 
<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a> function.

## -struct-fields

### -field dwTotalSize

Total size allocated to this data structure, in bytes.

### -field dwNeededSize

Size for this data structure that is needed to hold all the returned information, in bytes.

### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.

### -field dwNumLocations

Number of entries in the <b>LocationList</b>. It includes all locations defined, including zero (default).

### -field dwLocationListSize

Size of the list of locations known to the address translation, in bytes.

### -field dwLocationListOffset

Offset from the beginning of this structure to the list of locations known to the address translation. The list consists of a sequence of 
<a href="/windows/desktop/api/tapi/ns-tapi-linelocationentry">LINELOCATIONENTRY</a> structures. The <b>dwLocationListOffset</b> member points to the first byte of the first structure, and the <b>dwLocationListSize</b> member indicates the total number of bytes in the list.

### -field dwCurrentLocationID

Permanent identifier for the <b>CurrentLocation</b> entry in the [Locations] section of the registry. See the <b>dwPermanentLocationID</b> member of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linelocationentry">LINELOCATIONENTRY</a> structure.

### -field dwNumCards

Number of entries in the <b>CardList</b>.

### -field dwCardListSize

Size of the list of calling cards known to the address translation, in bytes.

### -field dwCardListOffset

Offset from the beginning of this structure to the list of calling cards known to the address translation. It includes only non-hidden card entries and always includes card 0 (direct dial). The list consists of a sequence of 
<a href="/windows/desktop/api/tapi/ns-tapi-linecardentry">LINECARDENTRY</a> structures. The <b>dwCardListOffset</b> member points to the first byte of the first structure, and the <b>dwCardListSize</b> member indicates the total number of bytes in the list.

### -field dwCurrentPreferredCardID

Preferred calling card for the <b>CurrentLocation</b> entry in the [Locations] section of the registry. See the <b>dwPreferredCardID</b> member of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linelocationentry">LINELOCATIONENTRY</a> structure.

## -remarks

This structure may not be extended.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linecardentry">LINECARDENTRY</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linelocationentry">LINELOCATIONENTRY</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a>