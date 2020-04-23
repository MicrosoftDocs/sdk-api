---
UID: NN:dwrite.IDWriteBitmapRenderTarget
title: IDWriteBitmapRenderTarget (dwrite.h)
description: Encapsulates a 32-bit device independent bitmap and device context, which can be used for rendering glyphs.helpviewer_keywords: ["IDWriteBitmapRenderTarget","IDWriteBitmapRenderTarget interface [Direct Write]","IDWriteBitmapRenderTarget interface [Direct Write]","described","directwrite.IDWriteBitmapRenderTarget","dwrite/IDWriteBitmapRenderTarget"]
old-location: directwrite\IDWriteBitmapRenderTarget.htm
tech.root: DirectWrite
ms.assetid: 9953a9e9-7772-41a3-9cd9-2340a9dd4b6f
ms.date: 12/05/2018
ms.keywords: IDWriteBitmapRenderTarget, IDWriteBitmapRenderTarget interface [Direct Write], IDWriteBitmapRenderTarget interface [Direct Write],described, directwrite.IDWriteBitmapRenderTarget, dwrite/IDWriteBitmapRenderTarget
f1_keywords:
- dwrite/IDWriteBitmapRenderTarget
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteBitmapRenderTarget
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteBitmapRenderTarget interface


## -description


 Encapsulates a 32-bit device independent bitmap and device context, which can be used for rendering glyphs.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteBitmapRenderTarget</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteBitmapRenderTarget</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteBitmapRenderTarget</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun">DrawGlyphRun</a>
</td>
<td align="left" width="63%">
 Draws a run of glyphs to a bitmap target at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getcurrenttransform">GetCurrentTransform</a>
</td>
<td align="left" width="63%">
 Gets the transform that maps abstract coordinates to DIPs. By default this is the identity 
     transform. Note that this is unrelated to the world transform of the underlying device
     context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc">GetMemoryDC</a>
</td>
<td align="left" width="63%">
 Gets a handle to the memory device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getpixelsperdip">GetPixelsPerDip</a>
</td>
<td align="left" width="63%">
 Gets the number of bitmap pixels per DIP. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getsize">GetSize</a>
</td>
<td align="left" width="63%">
 Gets the dimensions of the target bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-resize">Resize</a>
</td>
<td align="left" width="63%">
 Resizes the bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-setcurrenttransform">SetCurrentTransform</a>
</td>
<td align="left" width="63%">
 Sets the transform that maps abstract coordinate to DIPs (device-independent pixel). This does not affect the world
     transform of the underlying device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-setpixelsperdip">SetPixelsPerDip</a>
</td>
<td align="left" width="63%">
 Sets the number of bitmap pixels per DIP (device-independent pixel). A DIP is 1/96 inch, so this value is the number
     if pixels per inch divided by 96.

</td>
</tr>
</table> 


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



