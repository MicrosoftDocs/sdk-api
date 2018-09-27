---
UID: NS:tapi.varstring_tag
title: varstring_tag
author: windows-sdk-content
description: The VARSTRING structure is used for returning variably sized strings. It is used both by the line device class and the phone device class.
old-location: tapi2\varstring_str.htm
tech.root: tapi
ms.assetid: ec73ed48-db5a-4478-8748-b8e58247c2f4
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "*LPVARSTRING, LPVARSTRING, LPVARSTRING structure pointer [TAPI 2.2], VARSTRING, VARSTRING structure [TAPI 2.2], _tapi2_varstring_str, tapi/LPVARSTRING, tapi/VARSTRING, tapi2.varstring_str, varstring_tag"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - VARSTRING
product: Windows
targetos: Windows
req.typenames: VARSTRING, *LPVARSTRING
req.redist: 
---

# varstring_tag structure


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
<a href="https://msdn.microsoft.com/ca67c9d1-d3e0-4a55-9be7-6760edea96ee">STRINGFORMAT_ Constants</a>.


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


