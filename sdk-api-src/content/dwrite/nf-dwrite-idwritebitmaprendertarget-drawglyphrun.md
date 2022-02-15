---
UID: NF:dwrite.IDWriteBitmapRenderTarget.DrawGlyphRun
title: IDWriteBitmapRenderTarget::DrawGlyphRun (dwrite.h)
description: Draws a run of glyphs to a bitmap target at the specified position.
helpviewer_keywords: ["DrawGlyphRun","DrawGlyphRun method [Direct Write]","DrawGlyphRun method [Direct Write]","IDWriteBitmapRenderTarget interface","IDWriteBitmapRenderTarget interface [Direct Write]","DrawGlyphRun method","IDWriteBitmapRenderTarget.DrawGlyphRun","IDWriteBitmapRenderTarget::DrawGlyphRun","directwrite.IDWriteBitmapRenderTarget_DrawGlyphRun","dwrite/IDWriteBitmapRenderTarget::DrawGlyphRun"]
old-location: directwrite\IDWriteBitmapRenderTarget_DrawGlyphRun.htm
tech.root: DirectWrite
ms.assetid: d766d2d1-6be7-468a-a10e-c7cab421b9a7
ms.date: 12/05/2018
ms.keywords: DrawGlyphRun, DrawGlyphRun method [Direct Write], DrawGlyphRun method [Direct Write],IDWriteBitmapRenderTarget interface, IDWriteBitmapRenderTarget interface [Direct Write],DrawGlyphRun method, IDWriteBitmapRenderTarget.DrawGlyphRun, IDWriteBitmapRenderTarget::DrawGlyphRun, directwrite.IDWriteBitmapRenderTarget_DrawGlyphRun, dwrite/IDWriteBitmapRenderTarget::DrawGlyphRun
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
 - IDWriteBitmapRenderTarget::DrawGlyphRun
 - dwrite/IDWriteBitmapRenderTarget::DrawGlyphRun
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
 - IDWriteBitmapRenderTarget.DrawGlyphRun
---

# IDWriteBitmapRenderTarget::DrawGlyphRun


## -description

 Draws a run of glyphs to a bitmap target at the specified position.

## -parameters

### -param baselineOriginX

Type: <b>FLOAT</b>

The horizontal position of the baseline origin, in DIPs, relative to the upper-left corner of the DIB.

### -param baselineOriginY

Type: <b>FLOAT</b>

The vertical position of the baseline origin, in DIPs, relative to the upper-left corner of the DIB.

### -param measuringMode

Type: <b><a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE</a></b>

The measuring method for glyphs in the run, used with the other properties to determine the rendering mode.

### -param glyphRun [in]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run">DWRITE_GLYPH_RUN</a>*</b>

The structure containing the properties of the glyph run.

### -param renderingParams

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams">IDWriteRenderingParams</a>*</b>

The object that controls rendering behavior.

### -param textColor

Type: <b>COLORREF</b>

The foreground color of the text.

### -param blackBoxRect [out, optional]

Type: <b>RECT*</b>

The optional rectangle that receives the bounding box (in pixels not DIPs) of all the pixels affected by 
     drawing the glyph run. The black box rectangle may extend beyond the dimensions of the bitmap.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You can use the <b>IDWriteBitmapRenderTarget::DrawGlyphRun</b> to render to a bitmap from a custom text renderer that you implement.  The custom text renderer should call this method from within the <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun">IDWriteTextRenderer::DrawGlyphRun</a> callback method as shown in the following code.


```cpp
STDMETHODIMP GdiTextRenderer::DrawGlyphRun(
    __maybenull void* clientDrawingContext,
    FLOAT baselineOriginX,
    FLOAT baselineOriginY,
    DWRITE_MEASURING_MODE measuringMode,
    __in DWRITE_GLYPH_RUN const* glyphRun,
    __in DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription,
    IUnknown* clientDrawingEffect
    )
{
    HRESULT hr = S_OK;

    // Pass on the drawing call to the render target to do the real work.
    RECT dirtyRect = {0};

    hr = pRenderTarget_->DrawGlyphRun(
        baselineOriginX,
        baselineOriginY,
        measuringMode,
        glyphRun,
        pRenderingParams_,
        RGB(0,200,255),
        &dirtyRect
        );
    

    return hr;
}

```


The <i>baselineOriginX</i>, <i>baslineOriginY</i>, <i>measuringMethod</i>, and <i>glyphRun</i> parameters are provided (as arguments) when the callback method is invoked.  The <i>renderingParams</i>, <i>textColor</i> and <i>blackBoxRect</i> are not.

Default rendering params can be retrieved by using the <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams">IDWriteFactory::CreateMonitorRenderingParams</a> method.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget">IDWriteBitmapRenderTarget</a>

