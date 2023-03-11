---
UID: NE:d2d1svg.D2D1_SVG_PAINT_TYPE
title: D2D1_SVG_PAINT_TYPE (d2d1svg.h)
description: Specifies the paint type for an SVG fill or stroke.
helpviewer_keywords: ["D2D1_SVG_PAINT_TYPE","D2D1_SVG_PAINT_TYPE enumeration [Direct2D]","D2D1_SVG_PAINT_TYPE_COLOR","D2D1_SVG_PAINT_TYPE_CURRENT_COLOR","D2D1_SVG_PAINT_TYPE_FORCE_DWORD","D2D1_SVG_PAINT_TYPE_NONE","D2D1_SVG_PAINT_TYPE_URI","D2D1_SVG_PAINT_TYPE_URI_COLOR","D2D1_SVG_PAINT_TYPE_URI_CURRENT_COLOR","D2D1_SVG_PAINT_TYPE_URI_NONE","d2d1svg/D2D1_SVG_PAINT_TYPE","d2d1svg/D2D1_SVG_PAINT_TYPE_COLOR","d2d1svg/D2D1_SVG_PAINT_TYPE_CURRENT_COLOR","d2d1svg/D2D1_SVG_PAINT_TYPE_FORCE_DWORD","d2d1svg/D2D1_SVG_PAINT_TYPE_NONE","d2d1svg/D2D1_SVG_PAINT_TYPE_URI","d2d1svg/D2D1_SVG_PAINT_TYPE_URI_COLOR","d2d1svg/D2D1_SVG_PAINT_TYPE_URI_CURRENT_COLOR","d2d1svg/D2D1_SVG_PAINT_TYPE_URI_NONE","direct2d.d2d1_svg_paint_type"]
old-location: direct2d\d2d1_svg_paint_type.htm
tech.root: Direct2D
ms.assetid: FBCD7EF5-E1DF-4FE0-98A2-40F42798FB93
ms.date: 12/05/2018
ms.keywords: D2D1_SVG_PAINT_TYPE, D2D1_SVG_PAINT_TYPE enumeration [Direct2D], D2D1_SVG_PAINT_TYPE_COLOR, D2D1_SVG_PAINT_TYPE_CURRENT_COLOR, D2D1_SVG_PAINT_TYPE_FORCE_DWORD, D2D1_SVG_PAINT_TYPE_NONE, D2D1_SVG_PAINT_TYPE_URI, D2D1_SVG_PAINT_TYPE_URI_COLOR, D2D1_SVG_PAINT_TYPE_URI_CURRENT_COLOR, D2D1_SVG_PAINT_TYPE_URI_NONE, d2d1svg/D2D1_SVG_PAINT_TYPE, d2d1svg/D2D1_SVG_PAINT_TYPE_COLOR, d2d1svg/D2D1_SVG_PAINT_TYPE_CURRENT_COLOR, d2d1svg/D2D1_SVG_PAINT_TYPE_FORCE_DWORD, d2d1svg/D2D1_SVG_PAINT_TYPE_NONE, d2d1svg/D2D1_SVG_PAINT_TYPE_URI, d2d1svg/D2D1_SVG_PAINT_TYPE_URI_COLOR, d2d1svg/D2D1_SVG_PAINT_TYPE_URI_CURRENT_COLOR, d2d1svg/D2D1_SVG_PAINT_TYPE_URI_NONE, direct2d.d2d1_svg_paint_type
req.header: d2d1svg.h
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
req.typenames: D2D1_SVG_PAINT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_SVG_PAINT_TYPE
 - d2d1svg/D2D1_SVG_PAINT_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1svg.h
api_name:
 - D2D1_SVG_PAINT_TYPE
---

# D2D1_SVG_PAINT_TYPE enumeration


## -description

Specifies the paint type for an SVG fill or stroke.

## -enum-fields

### -field D2D1_SVG_PAINT_TYPE_NONE:0

The fill or stroke is not rendered.

### -field D2D1_SVG_PAINT_TYPE_COLOR:1

A solid color is rendered.

### -field D2D1_SVG_PAINT_TYPE_CURRENT_COLOR:2

The current color is rendered.

### -field D2D1_SVG_PAINT_TYPE_URI:3

A paint server, defined by another element in the SVG document, is used.

### -field D2D1_SVG_PAINT_TYPE_URI_NONE:4

A paint server, defined by another element in the SVG document, is used. If the paint server reference is invalid, fall back to D2D1_SVG_PAINT_TYPE_NONE.

### -field D2D1_SVG_PAINT_TYPE_URI_COLOR:5

A paint server, defined by another element in the SVG document, is used. If the paint server reference is invalid, fall back to D2D1_SVG_PAINT_TYPE_COLOR.

### -field D2D1_SVG_PAINT_TYPE_URI_CURRENT_COLOR:6

A paint server, defined by another element in the SVG document, is used. If the paint server reference is invalid, fall back to D2D1_SVG_PAINT_TYPE_CURRENT_COLOR.

### -field D2D1_SVG_PAINT_TYPE_FORCE_DWORD:0xffffffff

