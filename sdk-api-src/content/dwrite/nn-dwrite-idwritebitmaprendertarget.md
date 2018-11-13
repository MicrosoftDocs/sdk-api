---
UID: NN:dwrite.IDWriteBitmapRenderTarget
title: IDWriteBitmapRenderTarget
author: windows-sdk-content
description: Encapsulates a 32-bit device independent bitmap and device context, which can be used for rendering glyphs.
old-location: directwrite\IDWriteBitmapRenderTarget.htm
tech.root: DirectWrite
ms.assetid: 9953a9e9-7772-41a3-9cd9-2340a9dd4b6f
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IDWriteBitmapRenderTarget, IDWriteBitmapRenderTarget interface [Direct Write], IDWriteBitmapRenderTarget interface [Direct Write],described, directwrite.IDWriteBitmapRenderTarget, dwrite/IDWriteBitmapRenderTarget
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteBitmapRenderTarget interface


## -description


 Encapsulates a 32-bit device independent bitmap and device context, which can be used for rendering glyphs.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteBitmapRenderTarget</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteBitmapRenderTarget</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d766d2d1-6be7-468a-a10e-c7cab421b9a7">DrawGlyphRun</a>
</td>
<td align="left" width="63%">
 Draws a run of glyphs to a bitmap target at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f84e38e-f0e8-4cf7-bad0-d41f24ce9499">GetCurrentTransform</a>
</td>
<td align="left" width="63%">
 Gets the transform that maps abstract coordinates to DIPs. By default this is the identity 
     transform. Note that this is unrelated to the world transform of the underlying device
     context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ca9a002-2a78-4c7c-926c-52414dd801bb">GetMemoryDC</a>
</td>
<td align="left" width="63%">
 Gets a handle to the memory device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bf0488d-cc2e-4a95-8d95-f0bd8e5029d6">GetPixelsPerDip</a>
</td>
<td align="left" width="63%">
 Gets the number of bitmap pixels per DIP. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b73854c-674a-408a-8967-e72808ee296e">GetSize</a>
</td>
<td align="left" width="63%">
 Gets the dimensions of the target bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5686be35-bbc9-4d3a-a8a4-0277da7633b3">Resize</a>
</td>
<td align="left" width="63%">
 Resizes the bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/970092a4-e5f2-4795-aaf9-e0264a8b1845">SetCurrentTransform</a>
</td>
<td align="left" width="63%">
 Sets the transform that maps abstract coordinate to DIPs (device-independent pixel). This does not affect the world
     transform of the underlying device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da582190-4a6d-451a-9d42-831e8786570f">SetPixelsPerDip</a>
</td>
<td align="left" width="63%">
 Sets the number of bitmap pixels per DIP (device-independent pixel). A DIP is 1/96 inch, so this value is the number
     if pixels per inch divided by 96.

</td>
</tr>
</table> 


## -remarks



You create an <b>IDWriteBitmapRenderTarget</b> by using the <a href="https://msdn.microsoft.com/1a1bd200-6da6-4e4d-83d3-1f6a4a5e7152">IDWriteGdiInterop::CreateBitmapRenderTarget</a> method, as shown in the following code.


```cpp
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateBitmapRenderTarget(hdc, r.right, r.bottom, &g_pBitmapRenderTarget);
}

```



<a href="https://msdn.microsoft.com/1a1bd200-6da6-4e4d-83d3-1f6a4a5e7152">IDWriteGdiInterop::CreateBitmapRenderTarget</a> takes a handle to a DC and the desired width and height.  In the above example, the width and height given are the size of the window rect.

<h3><a id="Rendering"></a><a id="rendering"></a><a id="RENDERING"></a>Rendering</h3>
One way to use a  <b>IDWriteBitmapRenderTarget</b>, for rendering to a bitmap, is to implement a custom renderer interface derived from the <a href="https://msdn.microsoft.com/a2ac70c8-e33b-46f1-b53b-1ab07555f109">IDWriteTextRenderer</a> interface.  In your implementation of  the <a href="https://msdn.microsoft.com/95a0044c-dffd-4c6a-a6eb-2f87b02ef89a">DrawGlyphRun</a> method of your custom renderer, call the <a href="https://msdn.microsoft.com/d766d2d1-6be7-468a-a10e-c7cab421b9a7">IDWriteBitmapRenderTarget::DrawGlyphRun</a> method to draw the glyphs as shown in the following code.


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


The <b>IDWriteBitmapRenderTarget</b> encapsulates and renders to a bitmap in memory.  The  <a href="https://msdn.microsoft.com/9ca9a002-2a78-4c7c-926c-52414dd801bb">GetMemoryDC</a> function returns a handle to the device context of this bitmap.



