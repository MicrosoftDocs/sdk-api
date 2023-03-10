---
UID: NS:tapi.linecountryentry_tag
title: LINECOUNTRYENTRY (tapi.h)
description: Provides the data for a single country/region entry.
helpviewer_keywords: ["*LPLINECOUNTRYENTRY","LINECOUNTRYENTRY","LINECOUNTRYENTRY structure [TAPI 2.2]","LPLINECOUNTRYENTRY","LPLINECOUNTRYENTRY structure pointer [TAPI 2.2]","_tapi2_linecountryentry_str","tapi/LINECOUNTRYENTRY","tapi/LPLINECOUNTRYENTRY","tapi2.linecountryentry_str"]
old-location: tapi2\linecountryentry_str.htm
tech.root: tapi3
ms.assetid: 627ff743-f90b-4bcb-b646-cdbc9f768ad2
ms.date: 12/05/2018
ms.keywords: '*LPLINECOUNTRYENTRY, LINECOUNTRYENTRY, LINECOUNTRYENTRY structure [TAPI 2.2], LPLINECOUNTRYENTRY, LPLINECOUNTRYENTRY structure pointer [TAPI 2.2], _tapi2_linecountryentry_str, tapi/LINECOUNTRYENTRY, tapi/LPLINECOUNTRYENTRY, tapi2.linecountryentry_str'
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
req.typenames: LINECOUNTRYENTRY, *LPLINECOUNTRYENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - linecountryentry_tag
 - tapi/linecountryentry_tag
 - LPLINECOUNTRYENTRY
 - tapi/LPLINECOUNTRYENTRY
 - LINECOUNTRYENTRY
 - tapi/LINECOUNTRYENTRY
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
 - LINECOUNTRYENTRY
---

# LINECOUNTRYENTRY structure


## -description

The 
<b>LINECOUNTRYENTRY</b> structure provides the data for a single country/region entry. An array of one or more of these structures is part of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linecountrylist">LINECOUNTRYLIST</a> structure returned by the 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetcountry">lineGetCountry</a> function.

## -struct-fields

### -field dwCountryID

Country/region identifier of the entry. The country/region identifier is an internal identifier that allows multiple entries to exist in the country/region list with the same country/region code, for example, all countries or regions in North America and the Caribbean share the country/region code 1, but require separate entries in the list.

### -field dwCountryCode

Country/region code of the country/region represented by the entry; that is, the digits dialed in an international call. Only this value should be displayed to users. Country/region identifiers should never be displayed.

### -field dwNextCountryID

Country/region identifier of the next entry in the country/region list. Because country/region codes and identifiers are not assigned in any regular numeric sequence, the country/region list is a single linked list, with each entry pointing to the next. The last country/region in the list has a <b>dwNextCountryID</b> value of zero. When the 
<a href="/windows/desktop/api/tapi/ns-tapi-linecountrylist">LINECOUNTRYLIST</a> structure is used to obtain the entire list, the entries in the list are in sequence as linked by their <b>dwNextCountryID</b> members.

### -field dwCountryNameSize

Size, in bytes, of the name of the country/region including the <b>null</b> terminator.

### -field dwCountryNameOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string that specifies the name of the country/region. The size of the field is specified by <b>dwCountryNameSize</b>.

### -field dwSameAreaRuleSize

Size, in bytes, of the direct-dialed dialing rule including the <b>null</b> terminator.

### -field dwSameAreaRuleOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string that contains the dialing rule for direct-dialed calls to the same area code. The size of the field is specified by <b>dwSameAreaRuleSize</b>.

### -field dwLongDistanceRuleSize

Size, in bytes, of the long-distance dialing rule including the <b>null</b> terminator.

### -field dwLongDistanceRuleOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string that contains the dialing rule for direct-dialed calls to other areas in the same country/region. The size of the field is specified by <b>dwLongDistanceRuleSize</b>.

### -field dwInternationalRuleSize

Size, in bytes, of the international dialing rule including the <b>null</b> terminator.

### -field dwInternationalRuleOffset

Offset from the beginning of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linecountrylist">LINECOUNTRYLIST</a> structure to a <b>null</b>-terminated string that contains the dialing rule for direct-dialed calls to other countries/regions. The size of the field is specified by <b>dwInternationalRuleSize</b>.

## -remarks

This structure cannot be extended.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linecountrylist">LINECOUNTRYLIST</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetcountry">lineGetCountry</a>