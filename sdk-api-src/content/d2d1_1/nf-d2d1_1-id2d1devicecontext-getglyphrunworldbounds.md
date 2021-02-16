---
UID: NF:d2d1_1.ID2D1DeviceContext.GetGlyphRunWorldBounds
title: ID2D1DeviceContext::GetGlyphRunWorldBounds (d2d1_1.h)
description: Gets the world-space bounds in DIPs of the glyph run using the device context DPI.
helpviewer_keywords: ["GetGlyphRunWorldBounds","GetGlyphRunWorldBounds method [Direct2D]","GetGlyphRunWorldBounds method [Direct2D]","ID2D1DeviceContext interface","ID2D1DeviceContext interface [Direct2D]","GetGlyphRunWorldBounds method","ID2D1DeviceContext.GetGlyphRunWorldBounds","ID2D1DeviceContext::GetGlyphRunWorldBounds","d2d1_1/ID2D1DeviceContext::GetGlyphRunWorldBounds","direct2d.id2d1devicecontext_getglyphrunworldbounds"]
old-location: direct2d\id2d1devicecontext_getglyphrunworldbounds.htm
tech.root: Direct2D
ms.assetid: 1196095A-4B26-4E71-A7F4-86F23B79E1F6
ms.date: 12/05/2018
ms.keywords: GetGlyphRunWorldBounds, GetGlyphRunWorldBounds method [Direct2D], GetGlyphRunWorldBounds method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],GetGlyphRunWorldBounds method, ID2D1DeviceContext.GetGlyphRunWorldBounds, ID2D1DeviceContext::GetGlyphRunWorldBounds, d2d1_1/ID2D1DeviceContext::GetGlyphRunWorldBounds, direct2d.id2d1devicecontext_getglyphrunworldbounds
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DeviceContext::GetGlyphRunWorldBounds
 - d2d1_1/ID2D1DeviceContext::GetGlyphRunWorldBounds
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DeviceContext.GetGlyphRunWorldBounds
---

# ID2D1DeviceContext::GetGlyphRunWorldBounds


## -description

    Gets the world-space bounds in DIPs of the glyph run using the device
    context DPI.

## -parameters

### -param baselineOrigin

Type: <b><a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The origin of the baseline for the glyph run.

### -param glyphRun [in]

Type: <b>const <a href="/windows/desktop/api/dwrite/ns-dwrite-dwrite_glyph_run">DWRITE_GLYPH_RUN</a>*</b>

The glyph run to render.

### -param measuringMode

Type: <b><a href="/windows/desktop/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE</a></b>

The DirectWrite measuring mode that indicates how glyph metrics are used to measure text when it is formatted.

### -param bounds [out]

Type: <b><a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

The bounds of the glyph run in DIPs and in world space.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed to the returning function.</td>
</tr>
</table>

## -remarks

The image bounds reflect the current DPI, unit mode, and world transform of the context.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>