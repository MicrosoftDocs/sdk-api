---
UID: NS:tapi.varstring_tag
title: VARSTRING (tapi.h)
description: The VARSTRING structure is used for returning variably sized strings. It is used both by the line device class and the phone device class.
helpviewer_keywords: ["*LPVARSTRING","LPVARSTRING","LPVARSTRING structure pointer [TAPI 2.2]","VARSTRING","VARSTRING structure [TAPI 2.2]","_tapi2_varstring_str","tapi/LPVARSTRING","tapi/VARSTRING","tapi2.varstring_str"]
old-location: tapi2\varstring_str.htm
tech.root: tapi3
ms.assetid: ec73ed48-db5a-4478-8748-b8e58247c2f4
ms.date: 12/05/2018
ms.keywords: '*LPVARSTRING, LPVARSTRING, LPVARSTRING structure pointer [TAPI 2.2], VARSTRING, VARSTRING structure [TAPI 2.2], _tapi2_varstring_str, tapi/LPVARSTRING, tapi/VARSTRING, tapi2.varstring_str'
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
req.typenames: VARSTRING, *LPVARSTRING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - varstring_tag
 - tapi/varstring_tag
 - LPVARSTRING
 - tapi/LPVARSTRING
 - VARSTRING
 - tapi/VARSTRING
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
 - VARSTRING
---

# VARSTRING structure


## -description

The 
<b>VARSTRING</b> structure is used for returning variably sized strings. It is used both by the line device class and the phone device class.

## -struct-fields

### -field dwTotalSize

Total size allocated to this data structure, in bytes.

### -field dwNeededSize

Size for this data structure that is needed to hold all the returned information, in bytes.

### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.

### -field dwStringFormat

Format of the string. This member uses one of the 
<a href="/windows/desktop/Tapi/stringformat--constants">STRINGFORMAT_ Constants</a>.

### -field dwStringSize

Size of the string information, including the <b>null</b> terminator, in bytes.

### -field dwStringOffset

Offset from the beginning of the structure to the variably sized device field containing the string information. The size of the field is specified by <b>dwStringSize</b>.

## -remarks

No extensibility.

If a string cannot be returned in a variable structure, the <b>dwStringSize</b> and <b>dwStringOffset</b> members are set in one of the following ways:

<ul>
<li><b>dwStringSize</b> and <b>dwStringOffset</b> members are both set to zero.</li>
<li><b>dwStringOffset</b> is nonzero and <b>dwStringSize</b> is zero.</li>
<li><b>dwStringOffset</b> is nonzero, <b>dwStringSize</b> is 1, and the byte at the given offset is zero.</li>
</ul>