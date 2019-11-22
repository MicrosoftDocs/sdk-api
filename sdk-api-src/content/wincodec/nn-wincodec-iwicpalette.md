---
UID: NN:wincodec.IWICPalette
title: IWICPalette (wincodec.h)

description: Exposes methods for accessing and building a color table, primarily for indexed pixel formats.
old-location: wic\_wic_codec_iwicpalette.htm
tech.root: wic
ms.assetid: cb0e4f92-4aff-48c7-af62-5f7154539289

ms.date: 12/05/2018
ms.keywords: IWICPalette, IWICPalette interface [Windows Imaging Component], IWICPalette interface [Windows Imaging Component],described, _wic_codec_iwicpalette, wic._wic_codec_iwicpalette, wincodec/IWICPalette
ms.topic: interface
f1_keywords: 
 - "wincodec/IWICPalette"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICPalette
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICPalette interface


## -description


Exposes methods for accessing and building a color table, primarily for indexed pixel formats.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICPalette</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICPalette</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICPalette</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicpalette-getcolorcount">GetColorCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of colors in the color table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicpalette-getcolors">GetColors</a>
</td>
<td align="left" width="63%">
Fills out the supplied color array with the colors from the internal color table. The color array should be sized according to the return results from <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicpalette-getcolorcount">GetColorCount</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicpalette-gettype">GetType</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/ne-wincodec-wicbitmappalettetype">WICBitmapPaletteType</a> that describes the palette. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicpalette-hasalpha">HasAlpha</a>
</td>
<td align="left" width="63%">
Retrieves a value that describes whether the palette contains an alpha transparent color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicpalette-initializecustom">InitializeCustom</a>
</td>
<td align="left" width="63%">
Initializes a palette to the custom color entries provided.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicpalette-initializefrombitmap">InitializeFromBitmap</a>
</td>
<td align="left" width="63%">
Initializes a palette using a computed optimized values based on the reference bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicpalette-initializefrompalette">InitializeFromPalette</a>
</td>
<td align="left" width="63%">
Initialize the palette based on a given palette.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicpalette-initializepredefined">InitializePredefined</a>
</td>
<td align="left" width="63%">
Initializes the palette to one of the pre-defined palettes specified by <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/ne-wincodec-wicbitmappalettetype">WICBitmapPaletteType</a> and optionally adds a transparent color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicpalette-isblackwhite">IsBlackWhite</a>
</td>
<td align="left" width="63%">
Retrieves a value that describes whether the palette is black and white.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicpalette-isgrayscale">IsGrayscale</a>
</td>
<td align="left" width="63%">
Retrieves a value that describes whether a palette is grayscale.

</td>
</tr>
</table> 


## -remarks



If the <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/ne-wincodec-wicbitmappalettetype">WICBitmapPaletteType</a> is not <b>WICBitmapPaletteCustom</b>, then the colors are automatically generated based on the table above.  If the user subsequently changes a color palette entry the WICBitmapPalette is set to Custom by that action.


<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicpalette-initializefrombitmap">InitializeFromBitmap</a>'s <i>fAddTransparentColor</i> parameter will add a transparent color to the end of the color collection if its size if less than 256, otherwise index 255 will be replaced with the transparent color.  If a pre-defined palette type is used, it will change to BitmapPaletteTypeCustom since it no longer matches the predefined palette.

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

<pre class="syntax" xml:space="preserve"><code>0xAARRGGBB</code></pre>
The wincodec.h header type-defines <b>WICColor</b> as <b>UINT32</b>. 



