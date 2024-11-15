---
UID: NS:dwrite_3.DWRITE_FONT_AXIS_RANGE
title: DWRITE_FONT_AXIS_RANGE
description: Represents the minimum and maximum range of the possible values for a font axis.
helpviewer_keywords: ["DWRITE_FONT_AXIS_RANGE","DWRITE_FONT_AXIS_RANGE structure [Direct Write]","directwrite.dwrite_font_axis_range","dwrite_3/DWRITE_FONT_AXIS_RANGE"]
tech.root: DirectWrite
ms.date: 09/10/2019
ms.keywords: DWRITE_FONT_AXIS_RANGE, DWRITE_FONT_AXIS_RANGE structure [Direct Write], directwrite.dwrite_font_axis_range, dwrite_3/DWRITE_FONT_AXIS_RANGE
req.construct-type: structure
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
 - DWRITE_FONT_AXIS_RANGE
 - dwrite_3/DWRITE_FONT_AXIS_RANGE
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
 - DWRITE_FONT_AXIS_RANGE
---

## -description

Represents the minimum and maximum range of the possible values for a font axis. If *minValue* equals *maxValue*, then the axis is static rather than variable.

## -struct-fields

### -field axisTag

Type: **[DWRITE_FONT_AXIS_TAG](./ne-dwrite_3-dwrite_font_axis_tag.md)**

The four-character identifier of the font axis (for example, weight, width, slant, italic, and so on).

### -field minValue

Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**

The minimum value supported by this axis.

### -field maxValue

Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**

The maximum value supported by this axis.

## -remarks

The meaning and range of axis values depends on the semantics of the particular axis. Certain well-known axes have standard ranges and defaults. Here are some examples.

- Weight (1..1000, default == 400)
- Width (>0, default == 100)
- Slant (-90..90, default == -20)
- Italic (0 or 1)

## -see-also

[DWRITE_FONT_AXIS_TAG enumeration](./ne-dwrite_3-dwrite_font_axis_tag.md)

[DWRITE_FONT_AXIS_VALUE structure](./ns-dwrite_3-dwrite_font_axis_value.md)
