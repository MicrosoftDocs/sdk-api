---
UID: NF:dwrite_2.IDWriteTextRenderer1.DrawInlineObject
title: IDWriteTextRenderer1::DrawInlineObject (dwrite_2.h)
description: IDWriteTextLayout::Draw calls this application callback when it needs to draw an inline object. (IDWriteTextRenderer1.DrawInlineObject)
helpviewer_keywords: ["DrawInlineObject","DrawInlineObject method [Direct Write]","DrawInlineObject method [Direct Write]","IDWriteTextRenderer1 interface","IDWriteTextRenderer1 interface [Direct Write]","DrawInlineObject method","IDWriteTextRenderer1.DrawInlineObject","IDWriteTextRenderer1::DrawInlineObject","directwrite.idwritetextrenderer1_drawinlineobject","dwrite_2/IDWriteTextRenderer1::DrawInlineObject"]
old-location: directwrite\idwritetextrenderer1_drawinlineobject.htm
tech.root: DirectWrite
ms.assetid: 1115e215-d04e-28db-c196-7d693ca91044
ms.date: 12/05/2018
ms.keywords: DrawInlineObject, DrawInlineObject method [Direct Write], DrawInlineObject method [Direct Write],IDWriteTextRenderer1 interface, IDWriteTextRenderer1 interface [Direct Write],DrawInlineObject method, IDWriteTextRenderer1.DrawInlineObject, IDWriteTextRenderer1::DrawInlineObject, directwrite.idwritetextrenderer1_drawinlineobject, dwrite_2/IDWriteTextRenderer1::DrawInlineObject
req.header: dwrite_2.h
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteTextRenderer1::DrawInlineObject
 - dwrite_2/IDWriteTextRenderer1::DrawInlineObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteTextRenderer1.DrawInlineObject
---

# IDWriteTextRenderer1::DrawInlineObject


## -description

 IDWriteTextLayout::<a href="/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw">Draw</a> calls this application callback when it needs to
     draw an inline object.

## -parameters

### -param clientDrawingContext

Type: <b>void*</b>

The application-defined drawing context passed to IDWriteTextLayout::<a href="/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw">Draw</a>.

### -param originX

Type: <b>FLOAT</b>

X-coordinate at the top-left corner of the inline object.

### -param originY

Type: <b>FLOAT</b>

Y-coordinate at the top-left corner of the inline object.

### -param orientationAngle

Type: <b><a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_glyph_orientation_angle">DWRITE_GLYPH_ORIENTATION_ANGLE</a></b>

Orientation of the inline object.

### -param inlineObject

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject">IDWriteInlineObject</a>*</b>

The application-defined inline object set using <a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a>::<a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setinlineobject">SetInlineObject</a>.

### -param isSideways

Type: <b>BOOL</b>

A Boolean flag that indicates whether the object's baseline runs alongside the baseline axis of the line.

### -param isRightToLeft

Type: <b>BOOL</b>

A Boolean flag that indicates whether the object is in a right-to-left context, hinting that the drawing may want to mirror the normal image.

### -param clientDrawingEffect

Type: <b>IUnknown*</b>

Application-defined drawing effects for the glyphs to render. Usually this argument represents effects such as the foreground brush filling the interior of a line.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritetextrenderer1">IDWriteTextRenderer1</a>

