---
UID: NF:dwrite.IDWriteTextRenderer.DrawStrikethrough
title: IDWriteTextRenderer::DrawStrikethrough (dwrite.h)
description: IDWriteTextLayout::Draw calls this function to instruct the client to draw a strikethrough. (IDWriteTextRenderer.DrawStrikethrough)
helpviewer_keywords: ["DrawStrikethrough","DrawStrikethrough method [Direct Write]","DrawStrikethrough method [Direct Write]","IDWriteTextRenderer interface","IDWriteTextRenderer interface [Direct Write]","DrawStrikethrough method","IDWriteTextRenderer.DrawStrikethrough","IDWriteTextRenderer::DrawStrikethrough","directwrite.IDWriteTextRenderer_DrawStrikethrough","dwrite/IDWriteTextRenderer::DrawStrikethrough"]
old-location: directwrite\IDWriteTextRenderer_DrawStrikethrough.htm
tech.root: DirectWrite
ms.assetid: d7888c99-ff7c-4e14-b0a6-4726c9228226
ms.date: 12/05/2018
ms.keywords: DrawStrikethrough, DrawStrikethrough method [Direct Write], DrawStrikethrough method [Direct Write],IDWriteTextRenderer interface, IDWriteTextRenderer interface [Direct Write],DrawStrikethrough method, IDWriteTextRenderer.DrawStrikethrough, IDWriteTextRenderer::DrawStrikethrough, directwrite.IDWriteTextRenderer_DrawStrikethrough, dwrite/IDWriteTextRenderer::DrawStrikethrough
req.header: dwrite.h
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
 - IDWriteTextRenderer::DrawStrikethrough
 - dwrite/IDWriteTextRenderer::DrawStrikethrough
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
 - IDWriteTextRenderer.DrawStrikethrough
---

# IDWriteTextRenderer::DrawStrikethrough


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

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer">IDWriteTextRenderer</a>

