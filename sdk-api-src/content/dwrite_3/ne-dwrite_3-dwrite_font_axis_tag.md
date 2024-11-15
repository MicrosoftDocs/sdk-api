---
UID: NE:dwrite_3.DWRITE_FONT_AXIS_TAG
title: DWRITE_FONT_AXIS_TAG
description: Defines constants that specify a four-character identifier for a font axis.
helpviewer_keywords: ["DWRITE_FONT_AXIS_TAG","DWRITE_FONT_AXIS_TAG enumeration [Direct Write]","directwrite.dwrite_font_axis_tag","dwrite_3/DWRITE_FONT_AXIS_TAG"]
tech.root: DirectWrite
ms.date: 09/10/2019
ms.keywords: DWRITE_FONT_AXIS_TAG, DWRITE_FONT_AXIS_TAG enumeration [Direct Write], directwrite.dwrite_font_axis_tag, dwrite_3/DWRITE_FONT_AXIS_TAG
req.construct-type: enumeration
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 16299
req.target-min-winversvr: Windows 10 Build 16299
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
req.typenames: 
req.redist: 
f1_keywords:
 - DWRITE_FONT_AXIS_TAG
 - dwrite_3/DWRITE_FONT_AXIS_TAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite_3.h
api_name:
 - DWRITE_FONT_AXIS_TAG
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

[DWRITE_FONT_AXIS_RANGE structure](./ns-dwrite_3-dwrite_font_axis_range.md)
[DWRITE_FONT_AXIS_VALUE structure](./ns-dwrite_3-dwrite_font_axis_value.md)
