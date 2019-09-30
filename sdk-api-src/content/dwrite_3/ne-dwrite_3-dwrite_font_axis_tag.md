---
UID: NE:dwrite_3.DWRITE_FONT_AXIS_TAG
title: DWRITE_FONT_AXIS_TAG
author: windows-sdk-content
description: Defines constants that specify a four-character identifier for a font axis.
tech.root: DirectWrite
ms.author: windowssdkdev
ms.date: 09/10/2019
ms.keywords: DWRITE_FONT_AXIS_TAG, DWRITE_FONT_AXIS_TAG enumeration [Direct Write], directwrite.dwrite_font_axis_tag, dwrite_3/DWRITE_FONT_AXIS_TAG
ms.topic: enum
f1_keywords: 
 - "dwrite_3/DWRITE_FONT_AXIS_TAG"
req.construct-type: enumeration
req.header: dwrite_3.h
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
 - dwrite_3.h
api_name:
 - DWRITE_FONT_AXIS_TAG
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Defines constants that specify a four-character identifier for a font axis.

## -enum-fields

### -field DWRITE_FONT_AXIS_TAG_WEIGHT

Specifies the weight axis, using the identifier 'w','g','h','t'.

### -field DWRITE_FONT_AXIS_TAG_WIDTH

Specifies the width axis, using the identifier 'w','d','t','h'.

### -field DWRITE_FONT_AXIS_TAG_SLANT

Specifies the slant axis, using the identifier 's','l','n','t'.

### -field DWRITE_FONT_AXIS_TAG_OPTICAL_SIZE

Specifies the optical size axis, using the identifier 'o','p','s','z'.

### -field DWRITE_FONT_AXIS_TAG_ITALIC

Specifies the italic axis, using the identifier 'i','t','a','l'.

## -remarks

You can use the **DWRITE_MAKE_FONT_AXIS_TAG(a,b,c,d)** macro to create your own custom identifiers. Here's an example.

```cpp
DWRITE_MAKE_FONT_AXIS_TAG('c', 's', 't', 'm');
```

## -see-also

[DWRITE_FONT_AXIS_RANGE structure](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range)
[DWRITE_FONT_AXIS_VALUE structure](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value)