---
UID: NF:d2d1helper.BitmapBrushProperties
title: BitmapBrushProperties function (d2d1helper.h)
description: Creates a D2D1_BITMAP_BRUSH_PROPERTIES structure.
helpviewer_keywords: ["BitmapBrushProperties","BitmapBrushProperties function [Direct2D]","d2d1helper/BitmapBrushProperties","direct2d.bitmapbrushproperties"]
old-location: direct2d\bitmapbrushproperties.htm
tech.root: Direct2D
ms.assetid: 8945b4d8-0d6e-4f23-9a0b-1ec690339bdd
ms.date: 12/05/2018
ms.keywords: BitmapBrushProperties, BitmapBrushProperties function [Direct2D], d2d1helper/BitmapBrushProperties, direct2d.bitmapbrushproperties
req.header: d2d1helper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BitmapBrushProperties
 - d2d1helper/BitmapBrushProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - BitmapBrushProperties
---

# BitmapBrushProperties function


## -description

Creates a <a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties">D2D1_BITMAP_BRUSH_PROPERTIES</a> structure.

## -parameters

### -param extendModeX

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE</a></b>

A value that specifies how the brush horizontally tiles those areas that extend past its bitmap. The default value is <a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE CLAMP</a>.

### -param extendModeY

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE</a></b>

A value that specifies how the brush vertically tiles those areas that extend past its bitmap. The default value is <a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE CLAMP</a>.

### -param interpolationMode

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode">D2D1_BITMAP_INTERPOLATION_MODE</a></b>

A value that specifies the interpolation algorithm that is used when images are scaled or rotated. The default value is <a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode">D2D1_BITMAP_INTERPOLATION_MODE_LINEAR</a>.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties">D2D1_BITMAP_BRUSH_PROPERTIES</a></b>

A structure that describes the extend modes and the interpolation mode of an <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a>.

## -see-also

<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a>