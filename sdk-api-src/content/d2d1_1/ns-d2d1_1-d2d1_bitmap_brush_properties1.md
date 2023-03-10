---
UID: NS:d2d1_1.D2D1_BITMAP_BRUSH_PROPERTIES1
title: D2D1_BITMAP_BRUSH_PROPERTIES1 (d2d1_1.h)
description: Describes the extend modes and the interpolation mode of an ID2D1BitmapBrush. (D2D1_BITMAP_BRUSH_PROPERTIES1)
helpviewer_keywords: ["D2D1_BITMAP_BRUSH_PROPERTIES1","D2D1_BITMAP_BRUSH_PROPERTIES1 structure [Direct2D]","d2d1_1/D2D1_BITMAP_BRUSH_PROPERTIES1","direct2d.d2d1_bitmap_brush_properties1"]
old-location: direct2d\d2d1_bitmap_brush_properties1.htm
tech.root: Direct2D
ms.assetid: 0FECAD03-C35C-4729-9BBE-40DE11B34068
ms.date: 12/05/2018
ms.keywords: D2D1_BITMAP_BRUSH_PROPERTIES1, D2D1_BITMAP_BRUSH_PROPERTIES1 structure [Direct2D], d2d1_1/D2D1_BITMAP_BRUSH_PROPERTIES1, direct2d.d2d1_bitmap_brush_properties1
req.header: d2d1_1.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_BITMAP_BRUSH_PROPERTIES1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_BITMAP_BRUSH_PROPERTIES1
 - d2d1_1/D2D1_BITMAP_BRUSH_PROPERTIES1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1_1.h
api_name:
 - D2D1_BITMAP_BRUSH_PROPERTIES1
---

# D2D1_BITMAP_BRUSH_PROPERTIES1 structure


## -description

Describes the extend modes and the interpolation mode of an <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a>.

## -struct-fields

### -field extendModeX

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE</a></b>

A value that describes how the brush horizontally tiles those areas that extend past its bitmap.

### -field extendModeY

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE</a></b>

A value that describes how the brush vertically tiles those areas that extend past its bitmap.

### -field interpolationMode

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode">D2D1_INTERPOLATION_MODE</a></b>

A value that specifies how the bitmap is interpolated when it is scaled or rotated.

## -see-also

<a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode">D2D1_BITMAP_INTERPOLATION_MODE</a>



<a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE</a>
