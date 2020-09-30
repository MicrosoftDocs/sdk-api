---
UID: NS:tapi.phonebuttoninfo_tag
title: PHONEBUTTONINFO (tapi.h)
description: The PHONEBUTTONINFO structure contains information about a button on a phone device. This structure is used by multiple TAPI and TSPI functions.
helpviewer_keywords: ["*LPPHONEBUTTONINFO","LPPHONEBUTTONINFO","LPPHONEBUTTONINFO structure pointer [TAPI 2.2]","PHONEBUTTONINFO","PHONEBUTTONINFO structure [TAPI 2.2]","_tapi2_phonebuttoninfo_str","tapi/LPPHONEBUTTONINFO","tapi/PHONEBUTTONINFO","tapi2.phonebuttoninfo_str"]
old-location: tapi2\phonebuttoninfo_str.htm
tech.root: tapi3
ms.assetid: f8316587-f279-419a-a35d-194df3fc8383
ms.date: 12/05/2018
ms.keywords: '*LPPHONEBUTTONINFO, LPPHONEBUTTONINFO, LPPHONEBUTTONINFO structure pointer [TAPI 2.2], PHONEBUTTONINFO, PHONEBUTTONINFO structure [TAPI 2.2], _tapi2_phonebuttoninfo_str, tapi/LPPHONEBUTTONINFO, tapi/PHONEBUTTONINFO, tapi2.phonebuttoninfo_str'
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
req.typenames: PHONEBUTTONINFO, *LPPHONEBUTTONINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - phonebuttoninfo_tag
 - tapi/phonebuttoninfo_tag
 - LPPHONEBUTTONINFO
 - tapi/LPPHONEBUTTONINFO
 - PHONEBUTTONINFO
 - tapi/PHONEBUTTONINFO
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
 - PHONEBUTTONINFO
---

# PHONEBUTTONINFO structure


## -description

The 
<b>PHONEBUTTONINFO</b> structure contains information about a button on a phone device. This structure is used by multiple TAPI and TSPI functions.

## -struct-fields

### -field dwTotalSize

Total size allocated to this data structure, in bytes.

### -field dwNeededSize

Size for this data structure that is needed to hold all the returned information, in bytes.

### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.

### -field dwButtonMode

Mode or general usage class of the button. This member uses one of the 
<a href="/windows/desktop/Tapi/phonebuttonmode--constants">PHONEBUTTONMODE_ Constants</a>.

### -field dwButtonFunction

Function assigned to the button. This member uses one of the 
<a href="/windows/desktop/Tapi/phonebuttonfunction--constants">PHONEBUTTONFUNCTION_ Constants</a>.

### -field dwButtonTextSize

Size of the descriptive text for the button, in bytes.

### -field dwButtonTextOffset

Offset from the beginning of this structure to the variably sized field containing descriptive text for this button. The format of this information is as specified in the <b>dwStringFormat</b> member of the phone's device capabilities. The size of the field is specified by <b>dwButtonTextSize</b>.

### -field dwDevSpecificSize

Size of the device-specific field, in bytes. If the device-specific field is a pointer to a string, the size must include the <b>null</b> terminator.

### -field dwDevSpecificOffset

Offset from the beginning of the structure to the variably sized device-specific field. The size of the field is specified by <b>dwDevSpecificSize</b>.

### -field dwButtonState

For the 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetbuttoninfo">phoneGetButtonInfo</a> function, this field indicates the current state of the button, using the 
<a href="/windows/desktop/Tapi/phonebuttonstate--constants">PHONEBUTTONSTATE_ Constants</a>. This field is ignored by the 
<a href="/windows/desktop/api/tapi/nf-tapi-phonesetbuttoninfo">phoneSetButtonInfo</a> function.

## -remarks

Device-specific extensions should use the DevSpecific (<b>dwDevSpecificSize</b> and <b>dwDevSpecificOffset</b>) variably sized area of this data structure.

Older applications are compiled without this field in the 
<b>PHONEBUTTONINFO</b> structure, and using a SIZEOF PHONEBUTTONINFO smaller than the new size. The application passes in a <i>dwAPIVersion</i> parameter with the 
<a href="/windows/desktop/api/tapi/nf-tapi-phoneopen">phoneOpen</a> function, which can be used for guidance by TAPI in handling this situation. If the application passes in a <b>dwTotalSize</b> less than the size of the fixed portion of the structure as defined in the specified <b>dwAPIVersion</b>, PHONEERR_STRUCTURETOOSMALL is returned. If sufficient memory has been allocated by the application, before calling the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetbuttoninfo">TSPI_phoneGetButtonInfo</a> function, TAPI sets the <b>dwNeededSize</b> and <b>dwUsedSize</b> members to the fixed size of the structure as it existed in the specified API version.

New service providers (which support the new API version) must examine the API version passed in. If the API version is less than the highest version supported by the provider, the service provider must not fill in fields not supported in older API versions, as these would fall in the variable portion of the older structure.

New applications must be cognizant of the API version negotiated, and not examine the contents of fields in the fixed portion beyond the original end of the fixed portion of the structure for the negotiated API version.

## -see-also

<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetbuttoninfo">TSPI_phoneGetButtonInfo</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonesetbuttoninfo">TSPI_phoneSetButtonInfo</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonegetbuttoninfo">phoneGetButtonInfo</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phoneopen">phoneOpen</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonesetbuttoninfo">phoneSetButtonInfo</a>