---
UID: NN:wincodec.IWICPalette
title: IWICPalette (wincodec.h)
description: Exposes methods for accessing and building a color table, primarily for indexed pixel formats.
helpviewer_keywords: ["IWICPalette","IWICPalette interface [Windows Imaging Component]","IWICPalette interface [Windows Imaging Component]","described","_wic_codec_iwicpalette","wic._wic_codec_iwicpalette","wincodec/IWICPalette"]
old-location: wic\_wic_codec_iwicpalette.htm
tech.root: wic
ms.assetid: cb0e4f92-4aff-48c7-af62-5f7154539289
ms.date: 12/05/2018
ms.keywords: IWICPalette, IWICPalette interface [Windows Imaging Component], IWICPalette interface [Windows Imaging Component],described, _wic_codec_iwicpalette, wic._wic_codec_iwicpalette, wincodec/IWICPalette
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICPalette
 - wincodec/IWICPalette
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICPalette
---

# IWICPalette interface


## -description

Exposes methods for accessing and building a color table, primarily for indexed pixel formats.

## -inheritance

The <b>IWICPalette</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICPalette</b> also has these types of members:

## -remarks

If the <a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmappalettetype">WICBitmapPaletteType</a> is not <b>WICBitmapPaletteCustom</b>, then the colors are automatically generated based on the table above.  If the user subsequently changes a color palette entry the WICBitmapPalette is set to Custom by that action.


<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicpalette-initializefrombitmap">InitializeFromBitmap</a>'s <i>fAddTransparentColor</i> parameter will add a transparent color to the end of the color collection if its size if less than 256, otherwise index 255 will be replaced with the transparent color.  If a pre-defined palette type is used, it will change to BitmapPaletteTypeCustom since it no longer matches the predefined palette.

The palette interface is an auxiliary imaging interface in that it does not directly concern bitmaps and pixels; rather it provides indexed color translation for indexed bitmaps. For an indexed pixel format with M bits per pixels: (The number of colors in the palette) greater than 2^M.

Traditionally the basic operation of the palette is to provide a translation from a byte (or smaller) index into a 32bpp color value. This is often accomplished by a 256 entry table of color values.


#### Examples


```cpp
    IWICImagingFactory *pFactory = NULL;
    IWICBitmapDecoder *pDecoder = NULL;
    IWICBitmapFrameDecode *pBitmapFrameDecode = NULL;
    IWICPalette *pPalette = NULL;

    UINT uiFrameCount = 0;

    HRESULT hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWICImagingFactory,
        (LPVOID*)&pFactory
        );

    if (SUCCEEDED(hr))
    {
        hr = pFactory->CreateDecoderFromFilename(
                           L"test.gif",
                           NULL,
                           GENERIC_READ,
                           &pDecoder);
    }

    if (SUCCEEDED(hr))
    {
        hr = pDecoder->GetFrameCount(&uiFrameCount);
    }

    if (SUCCEEDED(hr) && (uiFrameCount > 0))
    {
        hr = pDecoder->GetFrame(0, &pBitmapFrameDecode);

        if (SUCCEEDED(hr))
        {
            hr = pFactory->CreatePalette(&pPalette);
        }

        if (SUCCEEDED(hr))
        {
            hr = pBitmapFrameDecode->CopyPalette(pPalette);
        }

        if (SUCCEEDED(hr))
        {
            UINT uiColorCount = 0;
            UINT uiActualColorCount = 0;
            WICColor *pColors = NULL;

            hr = pPalette->GetColorCount(&uiColorCount);

            if (SUCCEEDED(hr) && (uiColorCount > 0))
            {
                pColors = new WICColor[uiColorCount];

                if (pColors)
                {
                    hr = pPalette->GetColors(uiColorCount, pColors, &uiActualColorCount);

                    // Do something with the colors here...

                    delete[] pColors;
                }
                else
                {
                    hr = E_OUTOFMEMORY;
                }
            }
        }
    }

    if (pPalette)
    {
        pPalette->Release();
    }

    if (pBitmapFrameDecode)
    {
        pBitmapFrameDecode->Release();
    }

    if (pDecoder)
    {
        pDecoder->Release();
    }

    if (pFactory)
    {
        pFactory->Release();
    }

    return hr;
```


In this example code, <b>WICColor</b> is defined as a <b>UINT32</b> value with this layout: 


``` syntax
0xAARRGGBB
```

The wincodec.h header type-defines <b>WICColor</b> as <b>UINT32</b>.
