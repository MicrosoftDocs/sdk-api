---
UID: NN:dwrite.IDWriteBitmapRenderTarget
title: IDWriteBitmapRenderTarget (dwrite.h)
description: Encapsulates a 32-bit device independent bitmap and device context, which can be used for rendering glyphs.
helpviewer_keywords: ["IDWriteBitmapRenderTarget","IDWriteBitmapRenderTarget interface [Direct Write]","IDWriteBitmapRenderTarget interface [Direct Write]","described","directwrite.IDWriteBitmapRenderTarget","dwrite/IDWriteBitmapRenderTarget"]
old-location: directwrite\IDWriteBitmapRenderTarget.htm
tech.root: DirectWrite
ms.assetid: 9953a9e9-7772-41a3-9cd9-2340a9dd4b6f
ms.date: 12/05/2018
ms.keywords: IDWriteBitmapRenderTarget, IDWriteBitmapRenderTarget interface [Direct Write], IDWriteBitmapRenderTarget interface [Direct Write],described, directwrite.IDWriteBitmapRenderTarget, dwrite/IDWriteBitmapRenderTarget
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
 - IDWriteBitmapRenderTarget
 - dwrite/IDWriteBitmapRenderTarget
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
 - IDWriteBitmapRenderTarget
---

# IDWriteBitmapRenderTarget interface


## -description

 Encapsulates a 32-bit device independent bitmap and device context, which can be used for rendering glyphs.

## -inheritance

The <b>IDWriteBitmapRenderTarget</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteBitmapRenderTarget</b> also has these types of members:

## -remarks

You create an <b>IDWriteBitmapRenderTarget</b> by using the <a href="/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget">IDWriteGdiInterop::CreateBitmapRenderTarget</a> method, as shown in the following code.


```cpp
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateBitmapRenderTarget(hdc, r.right, r.bottom, &g_pBitmapRenderTarget);
}

```



<a href="/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget">IDWriteGdiInterop::CreateBitmapRenderTarget</a> takes a handle to a DC and the desired width and height.  In the above example, the width and height given are the size of the window rect.

<h3><a id="Rendering"></a><a id="rendering"></a><a id="RENDERING"></a>Rendering</h3>
One way to use a  <b>IDWriteBitmapRenderTarget</b>, for rendering to a bitmap, is to implement a custom renderer interface derived from the <a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer">IDWriteTextRenderer</a> interface.  In your implementation of  the <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun">DrawGlyphRun</a> method of your custom renderer, call the <a href="/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun">IDWriteBitmapRenderTarget::DrawGlyphRun</a> method to draw the glyphs as shown in the following code.


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


The <b>IDWriteBitmapRenderTarget</b> encapsulates and renders to a bitmap in memory.  The  <a href="/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc">GetMemoryDC</a> function returns a handle to the device context of this bitmap.

