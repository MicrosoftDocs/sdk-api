---
UID: NS:tapi.linetranslateoutput_tag
title: LINETRANSLATEOUTPUT (tapi.h)
description: The LINETRANSLATEOUTPUT structure describes the result of an address translation. The lineTranslateAddress function uses this structure.
helpviewer_keywords: ["*LPLINETRANSLATEOUTPUT","LINETRANSLATEOUTPUT","LINETRANSLATEOUTPUT structure [TAPI 2.2]","LPLINETRANSLATEOUTPUT","LPLINETRANSLATEOUTPUT structure pointer [TAPI 2.2]","_tapi2_linetranslateoutput_str","tapi/LINETRANSLATEOUTPUT","tapi/LPLINETRANSLATEOUTPUT","tapi2.linetranslateoutput_str"]
old-location: tapi2\linetranslateoutput_str.htm
tech.root: tapi3
ms.assetid: bcf094ad-8098-4e45-9131-25dbdb7e4093
ms.date: 12/05/2018
ms.keywords: '*LPLINETRANSLATEOUTPUT, LINETRANSLATEOUTPUT, LINETRANSLATEOUTPUT structure [TAPI 2.2], LPLINETRANSLATEOUTPUT, LPLINETRANSLATEOUTPUT structure pointer [TAPI 2.2], _tapi2_linetranslateoutput_str, tapi/LINETRANSLATEOUTPUT, tapi/LPLINETRANSLATEOUTPUT, tapi2.linetranslateoutput_str'
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
req.typenames: LINETRANSLATEOUTPUT, *LPLINETRANSLATEOUTPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - linetranslateoutput_tag
 - tapi/linetranslateoutput_tag
 - LPLINETRANSLATEOUTPUT
 - tapi/LPLINETRANSLATEOUTPUT
 - LINETRANSLATEOUTPUT
 - tapi/LINETRANSLATEOUTPUT
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
 - LINETRANSLATEOUTPUT
---

# LINETRANSLATEOUTPUT structure


## -description

The 
<b>LINETRANSLATEOUTPUT</b> structure describes the result of an address translation. The 
<a href="/windows/desktop/api/tapi/nf-tapi-linetranslateaddress">lineTranslateAddress</a> function uses this structure.

## -struct-fields

### -field dwTotalSize

Total size allocated to this data structure, in bytes.

### -field dwNeededSize

Size needed for this data structure to hold all the returned information, in bytes.

### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.

### -field dwDialableStringSize

Size dialable string, in bytes, including the terminating <b>NULL</b>.

### -field dwDialableStringOffset

Offset from the beginning of this structure to the translated output that can be passed to the 
<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a>, 
<a href="/windows/desktop/api/tapi/nf-tapi-linedial">lineDial</a>, or other function requiring a dialable string. The output is always a <b>null</b>-terminated string. Ancillary fields such as name and subaddress are included in this output string if they were in the input string. This string may contain private information such as calling card numbers. It should not be displayed to the user, to prevent inadvertent visibility to unauthorized persons. The size of the field is specified by <b>dwDialableStringSize</b>.

### -field dwDisplayableStringSize

Size of the translated output that can be displayed to the user, including the <b>null</b> terminator, in bytes.

### -field dwDisplayableStringOffset

Offset to the translated output that can be displayed to the user for confirmation. It is identical to <b>DialableString</b>, except the calling card digits are replaced with the friendly name of the card enclosed within bracket characters (for example, "[AT&amp;T Card]"), and ancillary fields such as name and subaddress are removed. Use an appropriate message in <b>dwDisplayableStringOffset</b>, because the string might be displayed publicly in the call-status dialog box. This information is also appropriate to include in call logs. The size of the field is specified by <b>dwDisplayableStringSize</b>.

### -field dwCurrentCountry

Country or region code configured in <b>CurrentLocation</b>. This value may be used to control the display by the application of certain user interface elements, for local call progress tone detection, and for other purposes.

### -field dwDestCountry

Destination country/region code of the translated address. This value may be passed to the <i>dwCountryCode</i> parameter of 
<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a> and other dialing functions (so that the call progress tones of the destination country/region such as a busy signal are properly detected). This field is set to zero if the destination address passed to 
<a href="/windows/desktop/api/tapi/nf-tapi-linetranslateaddress">lineTranslateAddress</a> is not in canonical format.

### -field dwTranslateResults

Information derived from the translation process, which may assist the application in presenting user-interface elements. This field uses one of the 
<a href="/windows/desktop/Tapi/linetranslateresult--constants">LINETRANSLATERESULT_ Constants</a>.

## -remarks

This structure cannot be extended.

## -see-also

<a href="/windows/desktop/api/tapi/nf-tapi-linedial">lineDial</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linetranslateaddress">lineTranslateAddress</a>