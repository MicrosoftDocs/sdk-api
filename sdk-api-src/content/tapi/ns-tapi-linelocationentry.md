---
UID: NS:tapi.linelocationentry_tag
title: LINELOCATIONENTRY (tapi.h)
description: Describes a location used to provide an address translation context.
helpviewer_keywords: ["*LPLINELOCATIONENTRY","LINELOCATIONENTRY","LINELOCATIONENTRY structure [TAPI 2.2]","LPLINELOCATIONENTRY","LPLINELOCATIONENTRY structure pointer [TAPI 2.2]","_tapi2_linelocationentry_str","tapi/LINELOCATIONENTRY","tapi/LPLINELOCATIONENTRY","tapi2.linelocationentry_str"]
old-location: tapi2\linelocationentry_str.htm
tech.root: tapi3
ms.assetid: 8b4357d8-6dc9-4fc8-b164-79675ac71870
ms.date: 12/05/2018
ms.keywords: '*LPLINELOCATIONENTRY, LINELOCATIONENTRY, LINELOCATIONENTRY structure [TAPI 2.2], LPLINELOCATIONENTRY, LPLINELOCATIONENTRY structure pointer [TAPI 2.2], _tapi2_linelocationentry_str, tapi/LINELOCATIONENTRY, tapi/LPLINELOCATIONENTRY, tapi2.linelocationentry_str'
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
req.typenames: LINELOCATIONENTRY, *LPLINELOCATIONENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - linelocationentry_tag
 - tapi/linelocationentry_tag
 - LPLINELOCATIONENTRY
 - tapi/LPLINELOCATIONENTRY
 - LINELOCATIONENTRY
 - tapi/LINELOCATIONENTRY
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
 - LINELOCATIONENTRY
---

# LINELOCATIONENTRY structure


## -description

The 
<b>LINELOCATIONENTRY</b> structure describes a location used to provide an address translation context. The 
<a href="/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a> structure can contain an array of 
<b>LINELOCATIONENTRY</b> structures.

## -struct-fields

### -field dwPermanentLocationID

Permanent. Identifies the location.

### -field dwLocationNameSize

Size, in characters,  of a <b>null</b>-terminated location name string including the <b>null</b>-terminating character.

### -field dwLocationNameOffset

Offset size, specified in  <b>dwLocationNameSize</b>, from the beginning of the <a href="/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a> structure (that contains this entry) to a <b>null</b>-terminated string that describes the location in a user-friendly manner.

### -field dwCountryCode

Country or region code of the location.

### -field dwCityCodeSize

Size, in characters, of the <b>null</b>-terminated city code string, including the <b>null</b>-terminating character.

### -field dwCityCodeOffset

Offset, specified in <b>dwCityCodeSize</b>,  from the beginning of this structure to a <b>null</b>-terminated string specifying the city/area code associated with the location. This information, with the country or region code, can be used by applications to "default" entry fields for the user when entering phone numbers, to encourage the entry of proper canonical numbers.

### -field dwPreferredCardID

Preferred calling card when dialing from this location.

### -field dwLocalAccessCodeSize

Size, in bytes, of the local access code string, including the <b>null</b> terminator.

### -field dwLocalAccessCodeOffset

Offset size, specified in <b>dwLocalAccessCodeSize</b>, from the beginning of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a> structure to a <b>null</b>-terminated string containing the access code to be dialed before calls to addresses in the local calling area.

### -field dwLongDistanceAccessCodeSize

Size, in bytes, of the long distance access code, including the <b>null</b> terminator.

### -field dwLongDistanceAccessCodeOffset

Offset size, specified in <b>dwLongDistanceAccessCodeSize</b>, from the beginning of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a> structure to a <b>null</b>-terminated string containing the access code to be dialed before calls to addresses outside the local calling area.

### -field dwTollPrefixListSize

Size, in bytes, of the toll prefix, including the <b>null</b> terminator.

### -field dwTollPrefixListOffset

Offset size, specified in <b>dwTollPrefixListSize</b>, from the beginning of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a> structure to a <b>null</b>-terminated string containing the toll prefix list for the location. The string contains only prefixes consisting of the digits "0" through "9", separated from each other by a single "," (comma) character.

### -field dwCountryID

Identifier of the country/region selected for the location. This can be used with the 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetcountry">lineGetCountry</a> function to obtain additional information about the specific country/region, such as the country/region name (the <b>dwCountryCode</b> member cannot be used for this purpose because country/region codes are not unique).

### -field dwOptions

Options in effect for this location, with values taken from the 
<a href="/windows/desktop/Tapi/linelocationoption--constants">LINELOCATIONOPTION_ Constants</a>.

### -field dwCancelCallWaitingSize

Size, in bytes, of the cancel-call-waiting string.

### -field dwCancelCallWaitingOffset

Offset size, specified in <b>dwCancelCallWaitingSize</b>, from the beginning of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a> structure to a <b>null</b>-terminated string containing the dial digits and modifier characters that should be prefixed to the dialable string (after the pulse/tone character) when an application sets the LINETRANSLATEOPTION_CANCELCALLWAITING bit in the <i>dwTranslateOptions</i> parameter of 
<a href="/windows/desktop/api/tapi/nf-tapi-linetranslateaddress">lineTranslateAddress</a>. If no prefix is defined, <b>dwCancelCallWaitingSize</b> may be set to zero, or 1, and <b>dwCancelCallWaitingOffset</b> may point to an empty string (single <b>NULL</b> byte).

## -remarks

This structure cannot be extended.

Older applications are compiled without knowledge of these new fields, and using a SIZEOF LINELOCATIONENTRY smaller than the new size. Because this is an array in the variable portion of a 
<a href="/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a> structure, it is imperative that older applications receive 
<b>LINELOCATIONENTRY</b> structures in the format they previously expected, or they are not able to index through the array properly. The application passes in a <i>dwAPIVersion</i> parameter with the 
<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a> function, which can be used for guidance by TAPI in handling this situation. The 
<b>lineGetTranslateCaps</b> function should use the 
<b>LINELOCATIONENTRY</b> members and size that match the indicated API version, when building the 
<a href="/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a> structure to be returned to the application.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetcountry">lineGetCountry</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linetranslateaddress">lineTranslateAddress</a>