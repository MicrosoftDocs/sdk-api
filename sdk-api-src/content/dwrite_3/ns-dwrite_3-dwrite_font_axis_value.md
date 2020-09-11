---
UID: NS:dwrite_3.DWRITE_FONT_AXIS_VALUE
title: DWRITE_FONT_AXIS_VALUE
description: Represents a value for a font axis. Used when querying and creating font instances.
helpviewer_keywords: ["DWRITE_FONT_AXIS_VALUE","DWRITE_FONT_AXIS_VALUE structure [Direct Write]","directwrite.dwrite_font_axis_value","dwrite_3/DWRITE_FONT_AXIS_VALUE"]
tech.root: DirectWrite
ms.date: 09/10/2019
ms.keywords: DWRITE_FONT_AXIS_VALUE, DWRITE_FONT_AXIS_VALUE structure [Direct Write], directwrite.dwrite_font_axis_value, dwrite_3/DWRITE_FONT_AXIS_VALUE
req.construct-type: structure
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
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - DWRITE_FONT_AXIS_VALUE
 - dwrite_3/DWRITE_FONT_AXIS_VALUE
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
 - DWRITE_FONT_AXIS_VALUE
---

## -description

Represents a value for a font axis. Used when querying and creating font instances (for example, see [IDWriteFontFace5::GetFontAxisValues](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontface5-getfontaxisvalues)).

## -struct-fields

### -field axisTag

Type: **[DWRITE_FONT_AXIS_TAG](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_tag)**

The four-character identifier of the font axis (for example, weight, width, slant, italic, and so on).

### -field value

Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**

A value for the axis specified in `axisTag`. The meaning and range of the value depends on the semantics of the particular axis. Certain well-known axes have standard ranges and defaults. Here are some examples.

- Weight (1..1000, default == 400)
- Width (>0, default == 100)
- Slant (-90..90, default == -20)
- Italic (0 or 1)

## -remarks

## -see-also

[DWRITE_FONT_AXIS_TAG enumeration](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_tag)

[DWRITE_FONT_AXIS_RANGE structure](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range)

