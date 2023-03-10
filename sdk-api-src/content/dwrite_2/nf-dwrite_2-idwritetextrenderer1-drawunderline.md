---
UID: NF:dwrite_2.IDWriteTextRenderer1.DrawUnderline
title: IDWriteTextRenderer1::DrawUnderline (dwrite_2.h)
description: IDWriteTextLayout::Draw calls this function to instruct the client to draw an underline. (IDWriteTextRenderer1.DrawUnderline)
helpviewer_keywords: ["DrawUnderline","DrawUnderline method [Direct Write]","DrawUnderline method [Direct Write]","IDWriteTextRenderer1 interface","IDWriteTextRenderer1 interface [Direct Write]","DrawUnderline method","IDWriteTextRenderer1.DrawUnderline","IDWriteTextRenderer1::DrawUnderline","directwrite.idwritetextrenderer1_drawunderline","dwrite_2/IDWriteTextRenderer1::DrawUnderline"]
old-location: directwrite\idwritetextrenderer1_drawunderline.htm
tech.root: DirectWrite
ms.assetid: c2c5ea68-c1d0-b467-a9a7-cb3a457ff68d
ms.date: 12/05/2018
ms.keywords: DrawUnderline, DrawUnderline method [Direct Write], DrawUnderline method [Direct Write],IDWriteTextRenderer1 interface, IDWriteTextRenderer1 interface [Direct Write],DrawUnderline method, IDWriteTextRenderer1.DrawUnderline, IDWriteTextRenderer1::DrawUnderline, directwrite.idwritetextrenderer1_drawunderline, dwrite_2/IDWriteTextRenderer1::DrawUnderline
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
 - IDWriteTextRenderer1::DrawUnderline
 - dwrite_2/IDWriteTextRenderer1::DrawUnderline
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
 - IDWriteTextRenderer1.DrawUnderline
---

# IDWriteTextRenderer1::DrawUnderline


## -description

 IDWriteTextLayout::<a href="/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw">Draw</a> calls this function to instruct the client to draw
     an underline.

## -parameters

### -param clientDrawingContext

Type: <b>void*</b>

The application-defined drawing context passed to 
     IDWriteTextLayout::<a href="/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw">Draw</a>.

### -param baselineOriginX

Type: <b>FLOAT</b>

The pixel location (X-coordinate) at the baseline origin of the run where underline applies.

### -param baselineOriginY

Type: <b>FLOAT</b>

The pixel location (Y-coordinate) at the baseline origin of the run where underline applies.

### -param orientationAngle

Type: <b><a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_glyph_orientation_angle">DWRITE_GLYPH_ORIENTATION_ANGLE</a></b>

Orientation of the underline.

### -param underline [in]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_underline">DWRITE_UNDERLINE</a>*</b>

Pointer to  a structure containing underline logical information.

### -param clientDrawingEffect

Type: <b>IUnknown*</b>

 Application-defined effect to apply to the underline. Usually this argument represents effects such as the foreground brush filling the interior of a line.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 A single underline can be broken into multiple calls, depending on
     how the formatting changes attributes. If font sizes/styles change
     within an underline, the thickness and offset will be averaged
     weighted according to characters.
     To get an appropriate starting pixel position, add underline::offset
     to the baseline. Otherwise there will be no spacing between the text.
     The x coordinate will always be passed as the left side, regardless
     of text directionality. This simplifies drawing and reduces the
     problem of round-off that could potentially cause gaps or a double
     stamped alpha blend. To avoid alpha overlap, round the end points
     to the nearest device pixel.

## -see-also

<a href="/windows/win32/api/dwrite_2/nn-dwrite_2-idwritetextrenderer1">IDWriteTextRenderer1</a>

