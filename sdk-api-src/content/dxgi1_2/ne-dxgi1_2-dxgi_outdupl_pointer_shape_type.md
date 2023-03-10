---
UID: NE:dxgi1_2.DXGI_OUTDUPL_POINTER_SHAPE_TYPE
title: DXGI_OUTDUPL_POINTER_SHAPE_TYPE (dxgi1_2.h)
description: Identifies the type of pointer shape.
helpviewer_keywords: ["DXGI_OUTDUPL_POINTER_SHAPE_TYPE","DXGI_OUTDUPL_POINTER_SHAPE_TYPE enumeration [DXGI]","DXGI_OUTDUPL_POINTER_SHAPE_TYPE_COLOR","DXGI_OUTDUPL_POINTER_SHAPE_TYPE_MASKED_COLOR","DXGI_OUTDUPL_POINTER_SHAPE_TYPE_MONOCHROME","direct3ddxgi.dxgi_outdupl_pointer_shape_type","dxgi1_2/DXGI_OUTDUPL_POINTER_SHAPE_TYPE","dxgi1_2/DXGI_OUTDUPL_POINTER_SHAPE_TYPE_COLOR","dxgi1_2/DXGI_OUTDUPL_POINTER_SHAPE_TYPE_MASKED_COLOR","dxgi1_2/DXGI_OUTDUPL_POINTER_SHAPE_TYPE_MONOCHROME"]
old-location: direct3ddxgi\dxgi_outdupl_pointer_shape_type.htm
tech.root: direct3ddxgi
ms.assetid: A066B6D3-A72A-48A9-BAED-BC3488BD1BC7
ms.date: 12/05/2018
ms.keywords: DXGI_OUTDUPL_POINTER_SHAPE_TYPE, DXGI_OUTDUPL_POINTER_SHAPE_TYPE enumeration [DXGI], DXGI_OUTDUPL_POINTER_SHAPE_TYPE_COLOR, DXGI_OUTDUPL_POINTER_SHAPE_TYPE_MASKED_COLOR, DXGI_OUTDUPL_POINTER_SHAPE_TYPE_MONOCHROME, direct3ddxgi.dxgi_outdupl_pointer_shape_type, dxgi1_2/DXGI_OUTDUPL_POINTER_SHAPE_TYPE, dxgi1_2/DXGI_OUTDUPL_POINTER_SHAPE_TYPE_COLOR, dxgi1_2/DXGI_OUTDUPL_POINTER_SHAPE_TYPE_MASKED_COLOR, dxgi1_2/DXGI_OUTDUPL_POINTER_SHAPE_TYPE_MONOCHROME
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DXGI_OUTDUPL_POINTER_SHAPE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_OUTDUPL_POINTER_SHAPE_TYPE
 - dxgi1_2/DXGI_OUTDUPL_POINTER_SHAPE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI1_2.h
api_name:
 - DXGI_OUTDUPL_POINTER_SHAPE_TYPE
---

# DXGI_OUTDUPL_POINTER_SHAPE_TYPE enumeration


## -description

Identifies the type of pointer shape.

## -enum-fields

### -field DXGI_OUTDUPL_POINTER_SHAPE_TYPE_MONOCHROME:0x1

The pointer type is a monochrome mouse pointer, which is  a monochrome bitmap. The bitmap's size is specified by width and height in a 1 bits per pixel (bpp) device independent bitmap (DIB) format AND mask that is followed by another 1 bpp DIB format XOR mask of the same size.

### -field DXGI_OUTDUPL_POINTER_SHAPE_TYPE_COLOR:0x2

The pointer type is a color mouse pointer, which is  a color bitmap. The bitmap's size is specified by width and height in a 32 bpp ARGB DIB format.

### -field DXGI_OUTDUPL_POINTER_SHAPE_TYPE_MASKED_COLOR:0x4

The pointer type is a masked color mouse pointer.  A masked color mouse pointer is a 32 bpp ARGB format bitmap with the mask value in the alpha bits. The only allowed mask values are 0 and 0xFF. When the mask value is 0, the RGB value should replace the screen pixel. When the mask value is 0xFF, an XOR operation is performed on the RGB value and the screen pixel; the result replaces the screen pixel.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-enums">DXGI Enumerations</a>



<a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_outdupl_pointer_shape_info">DXGI_OUTDUPL_POINTER_SHAPE_INFO</a>
