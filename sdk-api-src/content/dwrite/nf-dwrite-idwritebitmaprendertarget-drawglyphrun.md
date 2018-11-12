---
UID: NF:dwrite.IDWriteBitmapRenderTarget.DrawGlyphRun
title: IDWriteBitmapRenderTarget::DrawGlyphRun
author: windows-sdk-content
description: Draws a run of glyphs to a bitmap target at the specified position.
old-location: directwrite\IDWriteBitmapRenderTarget_DrawGlyphRun.htm
tech.root: DirectWrite
ms.assetid: d766d2d1-6be7-468a-a10e-c7cab421b9a7
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: DrawGlyphRun, DrawGlyphRun method [Direct Write], DrawGlyphRun method [Direct Write],IDWriteBitmapRenderTarget interface, IDWriteBitmapRenderTarget interface [Direct Write],DrawGlyphRun method, IDWriteBitmapRenderTarget.DrawGlyphRun, IDWriteBitmapRenderTarget::DrawGlyphRun, directwrite.IDWriteBitmapRenderTarget_DrawGlyphRun, dwrite/IDWriteBitmapRenderTarget::DrawGlyphRun
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IDWriteBitmapRenderTarget.DrawGlyphRun
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Type: <b><a href="https://msdn.microsoft.com/99e89754-8bc2-457d-bfdb-a3c9ccfe00c1">DWRITE_MEASURING_MODE</a></b>

The measuring method for glyphs in the run, used with the other properties to determine the rendering mode.


### -param glyphRun [in]

Type: <b>const <a href="https://msdn.microsoft.com/2997d63f-8d33-44c3-9617-cfffe5f61f7d">DWRITE_GLYPH_RUN</a>*</b>

The structure containing the properties of the glyph run.


### -param renderingParams

Type: <b><a href="https://msdn.microsoft.com/28b118e4-9a63-46cf-8ab7-e1039126405b">IDWriteRenderingParams</a>*</b>

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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can use the <b>IDWriteBitmapRenderTarget::DrawGlyphRun</b> to render to a bitmap from a custom text renderer that you implement.  The custom text renderer should call this method from within the <a href="https://msdn.microsoft.com/95a0044c-dffd-4c6a-a6eb-2f87b02ef89a">IDWriteTextRenderer::DrawGlyphRun</a> callback method as shown in the following code.


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

Default rendering params can be retrieved by using the <a href="https://msdn.microsoft.com/ddb6839a-9033-423a-a3f0-9352ec03e440">IDWriteFactory::CreateMonitorRenderingParams</a> method.






## -see-also




<a href="https://msdn.microsoft.com/9953a9e9-7772-41a3-9cd9-2340a9dd4b6f">IDWriteBitmapRenderTarget</a>
 

 

