---
UID: NF:d2d1_1helper.BitmapBrushProperties1
title: BitmapBrushProperties1 function (d2d1_1helper.h)
description: Creates a D2D1_BITMAP_BRUSH_PROPERTIES1 structure.
helpviewer_keywords: ["BitmapBrushProperties1","BitmapBrushProperties1 function [Direct2D]","d2d1_1helper/BitmapBrushProperties1","direct2d.bitmapbrushproperties1"]
old-location: direct2d\bitmapbrushproperties1.htm
tech.root: Direct2D
ms.assetid: 83F8641B-9BE4-4BBD-99FD-215EA3BD371A
ms.date: 12/05/2018
ms.keywords: BitmapBrushProperties1, BitmapBrushProperties1 function [Direct2D], d2d1_1helper/BitmapBrushProperties1, direct2d.bitmapbrushproperties1
req.header: d2d1_1helper.h
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
 - BitmapBrushProperties1
 - d2d1_1helper/BitmapBrushProperties1
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
 - BitmapBrushProperties1
---

# BitmapBrushProperties1 function


## -description

Creates a <a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_brush_properties1">D2D1_BITMAP_BRUSH_PROPERTIES1</a> structure.

## -parameters

### -param extendModeX

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE</a></b>

A value that specifies how the brush horizontally tiles those areas that extend past its bitmap. The default value is <a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE_CLAMP</a>.

### -param extendModeY

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE</a></b>

A value that specifies how the brush vertically tiles those areas that extend past its bitmap. The default value is <a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE_CLAMP</a>.

### -param interpolationMode

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode">D2D1_INTERPOLATION_MODE</a></b>

A value that specifies the interpolation algorithm that is used when images are scaled or rotated. The default value is <a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode">D2D1_INTERPOLATION_MODE_LINEAR</a>.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_brush_properties1">D2D1_BITMAP_BRUSH_PROPERTIES1</a></b>

A structure that describes the extend modes and the interpolation mode of an <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1">ID2D1BitmapBrush1</a>.