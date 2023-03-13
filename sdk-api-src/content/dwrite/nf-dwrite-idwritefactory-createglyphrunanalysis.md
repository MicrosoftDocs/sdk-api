---
UID: NF:dwrite.IDWriteFactory.CreateGlyphRunAnalysis
title: IDWriteFactory::CreateGlyphRunAnalysis (dwrite.h)
description: Creates a glyph run analysis object, which encapsulates information used to render a glyph run. (IDWriteFactory.CreateGlyphRunAnalysis)
helpviewer_keywords: ["CreateGlyphRunAnalysis","CreateGlyphRunAnalysis method [Direct Write]","CreateGlyphRunAnalysis method [Direct Write]","IDWriteFactory interface","IDWriteFactory interface [Direct Write]","CreateGlyphRunAnalysis method","IDWriteFactory.CreateGlyphRunAnalysis","IDWriteFactory::CreateGlyphRunAnalysis","directwrite.IDWriteFactory_CreateGlyphRunAnalysis","dwrite/IDWriteFactory::CreateGlyphRunAnalysis"]
old-location: directwrite\IDWriteFactory_CreateGlyphRunAnalysis.htm
tech.root: DirectWrite
ms.assetid: fcc6fe70-84ef-43ac-82ff-3f09d977220f
ms.date: 12/05/2018
ms.keywords: CreateGlyphRunAnalysis, CreateGlyphRunAnalysis method [Direct Write], CreateGlyphRunAnalysis method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateGlyphRunAnalysis method, IDWriteFactory.CreateGlyphRunAnalysis, IDWriteFactory::CreateGlyphRunAnalysis, directwrite.IDWriteFactory_CreateGlyphRunAnalysis, dwrite/IDWriteFactory::CreateGlyphRunAnalysis
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
 - IDWriteFactory::CreateGlyphRunAnalysis
 - dwrite/IDWriteFactory::CreateGlyphRunAnalysis
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
 - IDWriteFactory.CreateGlyphRunAnalysis
---

# IDWriteFactory::CreateGlyphRunAnalysis


## -description

 Creates a glyph run analysis object, which encapsulates information
     used to render a glyph run.

## -parameters

### -param glyphRun [in]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run">DWRITE_GLYPH_RUN</a>*</b>

A structure that contains the properties of the glyph run (font face, advances, and so on).

### -param pixelsPerDip

Type: <b>FLOAT</b>

Number of physical pixels per DIP (device independent pixel). For example, if rendering onto a 96 DPI bitmap then <i>pixelsPerDip</i> is 1. If rendering onto a 120 DPI bitmap then <i>pixelsPerDip</i> is 1.25.

### -param transform [in, optional]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix">DWRITE_MATRIX</a>*</b>

Optional transform applied to the glyphs and their positions. This transform is applied after the scaling specified the <i>emSize</i> and <i>pixelsPerDip</i>.

### -param renderingMode

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode">DWRITE_RENDERING_MODE</a></b>

A value that specifies the rendering mode, which must be one of the raster rendering modes (that is, not default
     and not outline).

### -param measuringMode

Type: <b><a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE</a></b>

Specifies the measuring mode to use with glyphs.

### -param baselineOriginX

Type: <b>FLOAT</b>

The horizontal position (X-coordinate) of the baseline origin, in DIPs.

### -param baselineOriginY

Type: <b>FLOAT</b>

Vertical position (Y-coordinate) of the baseline origin, in DIPs.

### -param glyphRunAnalysis [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis">IDWriteGlyphRunAnalysis</a>**</b>

When this method returns, contains an address of a pointer to the newly created glyph run analysis object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The glyph run analysis object contains the results of analyzing the glyph run, including the positions of all the glyphs and references to all of the rasterized glyphs in the font cache. 


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

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>

