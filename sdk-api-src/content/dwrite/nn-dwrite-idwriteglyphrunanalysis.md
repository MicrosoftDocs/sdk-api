---
UID: NN:dwrite.IDWriteGlyphRunAnalysis
title: IDWriteGlyphRunAnalysis (dwrite.h)
author: windows-sdk-content
description: Contains low-level information used to render a glyph run.
old-location: directwrite\IDWriteGlyphRunAnalysis.htm
tech.root: DirectWrite
ms.assetid: d4739b55-1a9b-4346-9b47-d8adb98df163
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteGlyphRunAnalysis, IDWriteGlyphRunAnalysis interface [Direct Write], IDWriteGlyphRunAnalysis interface [Direct Write],described, directwrite.IDWriteGlyphRunAnalysis, dwrite/IDWriteGlyphRunAnalysis
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
 - IDWriteGlyphRunAnalysis
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteGlyphRunAnalysis interface


## -description


 Contains low-level information used to render a glyph run.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteGlyphRunAnalysis</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteGlyphRunAnalysis</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteGlyphRunAnalysis</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3a28efa-b235-4608-8410-15cc0ebfe38e">CreateAlphaTexture</a>
</td>
<td align="left" width="63%">
 Creates an alpha texture of the specified type for glyphs within a specified bounding rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21991479-f041-40f9-83d5-0718ede26b92">GetAlphaBlendParams</a>
</td>
<td align="left" width="63%">
 Gets alpha blending properties required for ClearType blending.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9058edb7-23b2-418a-abcc-3ee827a79144">GetAlphaTextureBounds</a>
</td>
<td align="left" width="63%">
 Gets the bounding rectangle of the physical pixels affected by the glyph run.

</td>
</tr>
</table> 


## -remarks



The alpha texture can be a   bi-level alpha  texture or a ClearType alpha texture.  

A bi-level alpha texture contains one byte per pixel, therefore the size of the buffer for a bi-level texture will be the area of the texture bounds, in bytes. Each byte in a bi-level alpha texture created by <a href="https://msdn.microsoft.com/a3a28efa-b235-4608-8410-15cc0ebfe38e">CreateAlphaTexture</a> is either set to DWRITE_ALPHA_MAX (that is, 255) or zero.

A ClearType alpha texture contains three bytes per pixel, therefore the size of the buffer for a ClearType alpha texture is three times the area of the texture bounds, in bytes.


#### Examples

The following code example shows how to create a glyph run analysis object.  In this example, an empty glyph run is being used. 


```cpp
HRESULT CreateGlyphRunAnalysis(IDWriteFontFace *pFontFace, IDWriteGlyphRunAnalysis **ppGlyphRunAnalysis)
{
    HRESULT hr = S_OK;
    IDWriteFactory* pDWriteFactory = NULL;

    // Create the DirectWrite factory.
    hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory)
            );

    DWRITE_GLYPH_RUN emptyGlyphRun = { 0 };
    UINT16 glyphIndex = 0;
    
    emptyGlyphRun.fontFace = pFontFace;
    emptyGlyphRun.glyphIndices = &glyphIndex;
    emptyGlyphRun.glyphCount = 0;
   
    emptyGlyphRun.fontEmSize = 12;

    IDWriteGlyphRunAnalysis* pGlyphRunAnalysis = NULL;

    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory->CreateGlyphRunAnalysis(
            &emptyGlyphRun,
            1.0f, // pixelsPerDip,
            NULL, // transform,
            DWRITE_RENDERING_MODE_CLEARTYPE_GDI_CLASSIC,
            DWRITE_MEASURING_MODE_GDI_CLASSIC,
            0.0f, // baselineOriginX,
            0.0f, // baselineOriginY,
            &pGlyphRunAnalysis);
    }
    
    *ppGlyphRunAnalysis = pGlyphRunAnalysis;

    SafeRelease(&pDWriteFactory);

    return S_OK;
}

```




