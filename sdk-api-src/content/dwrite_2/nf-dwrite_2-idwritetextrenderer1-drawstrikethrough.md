---
UID: NF:dwrite_2.IDWriteTextRenderer1.DrawStrikethrough
title: IDWriteTextRenderer1::DrawStrikethrough (dwrite_2.h)
description: IDWriteTextLayout::Draw calls this function to instruct the client to draw a strikethrough. (IDWriteTextRenderer1.DrawStrikethrough)
helpviewer_keywords: ["DrawStrikethrough","DrawStrikethrough method [Direct Write]","DrawStrikethrough method [Direct Write]","IDWriteTextRenderer1 interface","IDWriteTextRenderer1 interface [Direct Write]","DrawStrikethrough method","IDWriteTextRenderer1.DrawStrikethrough","IDWriteTextRenderer1::DrawStrikethrough","directwrite.idwritetextrenderer1_drawstrikethrough","dwrite_2/IDWriteTextRenderer1::DrawStrikethrough"]
old-location: directwrite\idwritetextrenderer1_drawstrikethrough.htm
tech.root: DirectWrite
ms.assetid: 8800a536-9477-89c5-c48d-3f4bdf1ca1a5
ms.date: 12/05/2018
ms.keywords: DrawStrikethrough, DrawStrikethrough method [Direct Write], DrawStrikethrough method [Direct Write],IDWriteTextRenderer1 interface, IDWriteTextRenderer1 interface [Direct Write],DrawStrikethrough method, IDWriteTextRenderer1.DrawStrikethrough, IDWriteTextRenderer1::DrawStrikethrough, directwrite.idwritetextrenderer1_drawstrikethrough, dwrite_2/IDWriteTextRenderer1::DrawStrikethrough
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
 - IDWriteTextRenderer1::DrawStrikethrough
 - dwrite_2/IDWriteTextRenderer1::DrawStrikethrough
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
 - IDWriteTextRenderer1.DrawStrikethrough
---

# IDWriteTextRenderer1::DrawStrikethrough


## -description

 IDWriteTextLayout::<a href="/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw">Draw</a> calls this function to instruct the client to draw
     a strikethrough.

## -parameters

### -param clientDrawingContext

Type: <b>void*</b>

The application-defined drawing context passed to 
     IDWriteTextLayout::<a href="/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw">Draw</a>.

### -param baselineOriginX

Type: <b>FLOAT</b>

The pixel location (X-coordinate) at the baseline origin of the run where strikethrough applies.

### -param baselineOriginY

Type: <b>FLOAT</b>

The pixel location (Y-coordinate) at the baseline origin of the run where strikethrough applies.

### -param orientationAngle

Type: <b><a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_glyph_orientation_angle">DWRITE_GLYPH_ORIENTATION_ANGLE</a></b>

Orientation of the strikethrough.

### -param strikethrough [in]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_strikethrough">DWRITE_STRIKETHROUGH</a>*</b>

Pointer to  a structure containing strikethrough logical information.

### -param clientDrawingEffect

Type: <b>IUnknown*</b>

Application-defined effect to apply to the strikethrough.  Usually this argument represents effects such as the foreground brush filling the interior of a line.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 A single strikethrough can be broken into multiple calls, depending on
     how the formatting changes attributes. Strikethrough is not averaged
     across font sizes/styles changes.
     To get an appropriate starting pixel position, add strikethrough::offset
     to the baseline.
     Like underlines, the x coordinate will always be passed as the left side,
     regardless of text directionality.

## -see-also

<a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritetextrenderer1">IDWriteTextRenderer1</a>

