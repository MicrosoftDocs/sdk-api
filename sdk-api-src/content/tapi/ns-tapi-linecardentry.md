---
UID: NS:tapi.linecardentry_tag
title: LINECARDENTRY (tapi.h)
description: The LINECARDENTRY structure describes a calling card. The LINETRANSLATECAPS structure can contain an array of LINECARDENTRY structures.
helpviewer_keywords: ["*LPLINECARDENTRY","LINECARDENTRY","LINECARDENTRY structure [TAPI 2.2]","LPLINECARDENTRY","LPLINECARDENTRY structure pointer [TAPI 2.2]","_tapi2_linecardentry_str","tapi/LINECARDENTRY","tapi/LPLINECARDENTRY","tapi2.linecardentry_str"]
old-location: tapi2\linecardentry_str.htm
tech.root: tapi3
ms.assetid: 8b2a4eaf-6c59-4d3b-839f-52915bff6116
ms.date: 12/05/2018
ms.keywords: '*LPLINECARDENTRY, LINECARDENTRY, LINECARDENTRY structure [TAPI 2.2], LPLINECARDENTRY, LPLINECARDENTRY structure pointer [TAPI 2.2], _tapi2_linecardentry_str, tapi/LINECARDENTRY, tapi/LPLINECARDENTRY, tapi2.linecardentry_str'
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
req.typenames: LINECARDENTRY, *LPLINECARDENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - linecardentry_tag
 - tapi/linecardentry_tag
 - LPLINECARDENTRY
 - tapi/LPLINECARDENTRY
 - LINECARDENTRY
 - tapi/LINECARDENTRY
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
 - LINECARDENTRY
---

# LINECARDENTRY structure


## -description

The 
<b>LINECARDENTRY</b> structure describes a calling card. The 
<a href="/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a> structure can contain an array of 
<b>LINECARDENTRY</b> structures.

## -struct-fields

### -field dwPermanentCardID

Permanent identifier that identifies the card.

### -field dwCardNameSize

Size of the card name string including <b>null</b> terminator, in bytes.

### -field dwCardNameOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string that describes the card in a user-friendly manner. The size of the field is specified by <b>dwCardNameSize</b>.

### -field dwCardNumberDigits

Number of digits in the existing card number. The card number itself is not returned for security reasons (it is stored in scrambled form by TAPI). The application can use this to insert filler bytes into a text control in "password" mode to show that a number exists.

### -field dwSameAreaRuleSize

Size of the same-area dialing rule including the <b>null</b> terminator, in bytes.

### -field dwSameAreaRuleOffset

Offset from the beginning of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a> structure to the dialing rule defined for calls to numbers in the same area code. The rule is a <b>null</b>-terminated string. The size of the field is specified by <b>dwSameAreaRuleSize</b>.

### -field dwLongDistanceRuleSize

Size of the long distance dialing rule including the <b>null</b> terminator, in bytes.

### -field dwLongDistanceRuleOffset

Offset from the beginning of the structure to the dialing rule defined for calls to numbers in the other areas in the same country/region. The rule is a <b>null</b>-terminated string. The size of the field is specified by <b>dwLongDistanceRuleSize</b>.

### -field dwInternationalRuleSize

Size of the international dialing rule including the <b>null</b> terminator, in bytes.

### -field dwInternationalRuleOffset

Offset from the beginning of the structure to the dialing rule defined for calls to numbers in other countries/regions. The rule is a <b>null</b>-terminated string. The size of the field is specified by <b>dwInternationalRuleSize</b>.

### -field dwOptions

Indicates other settings associated with this calling card, using the 
<a href="/windows/desktop/Tapi/linecardoption--constants">LINECARDOPTION_ Constants</a>.

## -remarks

Older applications are compiled without knowledge of these new fields, and using a SIZEOF(LINECARDENTRY) smaller than the new size. Because this is an array in the variable portion of a 
<a href="/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a> structure, it is imperative that older applications receive 
<b>LINECARDENTRY</b> structures in the format they previously expected, or they are not able to index properly through the array. The application passes in a <i>dwAPIVersion</i> parameter with the 
<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a> function, which can be used for guidance by TAPI in handling this situation. The 
<b>lineGetTranslateCaps</b> function should use the 
<b>LINECARDENTRY</b> fields and size that match the indicated API version, when building the 
<a href="/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a> structure to be returned to the application.

This structure may not be extended.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a>