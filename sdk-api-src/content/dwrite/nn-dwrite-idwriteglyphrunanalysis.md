---
UID: NN:dwrite.IDWriteGlyphRunAnalysis
title: IDWriteGlyphRunAnalysis (dwrite.h)
description: Contains low-level information used to render a glyph run.
helpviewer_keywords: ["IDWriteGlyphRunAnalysis","IDWriteGlyphRunAnalysis interface [Direct Write]","IDWriteGlyphRunAnalysis interface [Direct Write]","described","directwrite.IDWriteGlyphRunAnalysis","dwrite/IDWriteGlyphRunAnalysis"]
old-location: directwrite\IDWriteGlyphRunAnalysis.htm
tech.root: DirectWrite
ms.assetid: d4739b55-1a9b-4346-9b47-d8adb98df163
ms.date: 12/05/2018
ms.keywords: IDWriteGlyphRunAnalysis, IDWriteGlyphRunAnalysis interface [Direct Write], IDWriteGlyphRunAnalysis interface [Direct Write],described, directwrite.IDWriteGlyphRunAnalysis, dwrite/IDWriteGlyphRunAnalysis
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
 - IDWriteGlyphRunAnalysis
 - dwrite/IDWriteGlyphRunAnalysis
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
 - IDWriteGlyphRunAnalysis
---

# IDWriteGlyphRunAnalysis interface


## -description

 Contains low-level information used to render a glyph run.

## -inheritance

The <b>IDWriteGlyphRunAnalysis</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteGlyphRunAnalysis</b> also has these types of members:

## -remarks

The alpha texture can be a   bi-level alpha  texture or a ClearType alpha texture.  

A bi-level alpha texture contains one byte per pixel, therefore the size of the buffer for a bi-level texture will be the area of the texture bounds, in bytes. Each byte in a bi-level alpha texture created by <a href="/windows/win32/api/dwrite/nf-dwrite-idwriteglyphrunanalysis-createalphatexture">CreateAlphaTexture</a> is either set to DWRITE_ALPHA_MAX (that is, 255) or zero.

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

