---
UID: NE:dwrite_3.DWRITE_FONT_AXIS_ATTRIBUTES
title: DWRITE_FONT_AXIS_ATTRIBUTES
description: Defines constants that specify attributes for a font axis.
helpviewer_keywords: ["DWRITE_FONT_AXIS_ATTRIBUTES","DWRITE_FONT_AXIS_ATTRIBUTES enumeration [Direct Write]","directwrite.dwrite_font_axis_attributes","dwrite_3/DWRITE_FONT_AXIS_ATTRIBUTES"]
tech.root: DirectWrite
ms.date: 09/16/2019
ms.keywords: DWRITE_FONT_AXIS_ATTRIBUTES, DWRITE_FONT_AXIS_ATTRIBUTES enumeration [Direct Write], directwrite.dwrite_font_axis_attributes, dwrite_3/DWRITE_FONT_AXIS_ATTRIBUTES
req.construct-type: enumeration
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
 - DWRITE_FONT_AXIS_ATTRIBUTES
 - dwrite_3/DWRITE_FONT_AXIS_ATTRIBUTES
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
 - DWRITE_FONT_AXIS_ATTRIBUTES
---

## -description

Defines constants that specify attributes for a font axis. Values can be bitwise OR'd together.

## -enum-fields

### -field DWRITE_FONT_AXIS_ATTRIBUTES_NONE:0x0000

Specifies no attributes.

### -field DWRITE_FONT_AXIS_ATTRIBUTES_VARIABLE:0x0001

Specifies that this axis is implemented as a variation axis in a variable font, with a continuous range of values, such as a range of weights from 100..900. Otherwise, it is either a static axis that holds a single point, or it has a range but doesn't vary, such as optical size in the Skia Heading font (which covers a range of points but doesn't interpolate any new glyph outlines).

### -field DWRITE_FONT_AXIS_ATTRIBUTES_HIDDEN:0x0002

Specifies that this axis is recommended to be remain hidden in user interfaces. The font developer may recommend this if an axis is intended to be accessed only programmatically, or is meant for font-internal or font-developer use only. The axis may be exposed in lower-level font inspection utilities, but should not be exposed in common nor even advanced-mode user interfaces in content-authoring apps.

## -remarks

## -see-also

