---
UID: NN:wincodec.IWICPalette
title: IWICPalette
author: windows-sdk-content
description: Exposes methods for accessing and building a color table, primarily for indexed pixel formats.
old-location: wic\_wic_codec_iwicpalette.htm
old-project: wic
ms.assetid: cb0e4f92-4aff-48c7-af62-5f7154539289
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IWICPalette, IWICPalette interface [Windows Imaging Component], IWICPalette interface [Windows Imaging Component],described, _wic_codec_iwicpalette, wic._wic_codec_iwicpalette, wincodec/IWICPalette
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: WICTiffCompressionOption
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICPalette
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICPalette interface


## -description


Exposes methods for accessing and building a color table, primarily for indexed pixel formats.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICPalette</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICPalette</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/133ee983-8df2-4053-aa8a-471aa679b412">GetColorCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of colors in the color table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/efec97fd-251c-4e52-b92e-4e624cdb9881">GetColors</a>
</td>
<td align="left" width="63%">
Fills out the supplied color array with the colors from the internal color table. The color array should be sized according to the return results from <a href="https://msdn.microsoft.com/133ee983-8df2-4053-aa8a-471aa679b412">GetColorCount</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991813">GetType</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/a8192905-2bae-4760-bf2d-64640c46e168">WICBitmapPaletteType</a> that describes the palette. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c2cd523-04e4-4f19-b7f3-cc2af7604283">HasAlpha</a>
</td>
<td align="left" width="63%">
Retrieves a value that describes whether the palette contains an alpha transparent color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eef17030-13eb-4d59-ac47-a49ffe2c80c8">InitializeCustom</a>
</td>
<td align="left" width="63%">
Initializes a palette to the custom color entries provided.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f17d0f16-729e-466c-902f-61398daf2921">InitializeFromBitmap</a>
</td>
<td align="left" width="63%">
Initializes a palette using a computed optimized values based on the reference bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1e27b1a-5103-4111-8356-f35d53a07f4b">InitializeFromPalette</a>
</td>
<td align="left" width="63%">
Initialize the palette based on a given palette.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/507888ad-4e3f-4e31-83c4-63a473eb7681">InitializePredefined</a>
</td>
<td align="left" width="63%">
Initializes the palette to one of the pre-defined palettes specified by <a href="https://msdn.microsoft.com/a8192905-2bae-4760-bf2d-64640c46e168">WICBitmapPaletteType</a> and optionally adds a transparent color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a22603b9-5c23-4016-9f28-1cf420ac11fa">IsBlackWhite</a>
</td>
<td align="left" width="63%">
Retrieves a value that describes whether the palette is black and white.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a559fa20-a967-4f8f-b978-f36365d3f00a">IsGrayscale</a>
</td>
<td align="left" width="63%">
Retrieves a value that describes whether a palette is grayscale.

</td>
</tr>
</table> 


## -remarks



If the <a href="https://msdn.microsoft.com/a8192905-2bae-4760-bf2d-64640c46e168">WICBitmapPaletteType</a> is not <b>WICBitmapPaletteCustom</b>, then the colors are automatically generated based on the table above.  If the user subsequently changes a color palette entry the WICBitmapPalette is set to Custom by that action.


<a href="https://msdn.microsoft.com/f17d0f16-729e-466c-902f-61398daf2921">InitializeFromBitmap</a>'s <i>fAddTransparentColor</i> parameter will add a transparent color to the end of the color collection if its size if less than 256, otherwise index 255 will be replaced with the transparent color.  If a pre-defined palette type is used, it will change to BitmapPaletteTypeCustom since it no longer matches the predefined palette.

The palette interface is an auxiliary imaging interface in that it does not directly concern bitmaps and pixels; rather it provides indexed color translation for indexed bitmaps. For an indexed pixel format with M bits per pixels: (The number of colors in the palette) greater than 2^M.

Traditionally the basic operation of the palette is to provide a translation from a byte (or smaller) index into a 32bpp color value. This is often accomplished by a 256 entry table of color values.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    IWICImagingFactory *pFactory = NULL;
    IWICBitmapDecoder *pDecoder = NULL;
    IWICBitmapFrameDecode *pBitmapFrameDecode = NULL;
    IWICPalette *pPalette = NULL;

    UINT uiFrameCount = 0;

    HRESULT hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWICImagingFactory,
        (LPVOID*)&amp;pFactory
        );

    if (SUCCEEDED(hr))
    {
        hr = pFactory-&gt;CreateDecoderFromFilename(
                           L"test.gif",
                           NULL,
                           GENERIC_READ,
                           &amp;pDecoder);
    }

    if (SUCCEEDED(hr))
    {
        hr = pDecoder-&gt;GetFrameCount(&amp;uiFrameCount);
    }

    if (SUCCEEDED(hr) &amp;&amp; (uiFrameCount &gt; 0))
    {
        hr = pDecoder-&gt;GetFrame(0, &amp;pBitmapFrameDecode);

        if (SUCCEEDED(hr))
        {
            hr = pFactory-&gt;CreatePalette(&amp;pPalette);
        }

        if (SUCCEEDED(hr))
        {
            hr = pBitmapFrameDecode-&gt;CopyPalette(pPalette);
        }

        if (SUCCEEDED(hr))
        {
            UINT uiColorCount = 0;
            UINT uiActualColorCount = 0;
            WICColor *pColors = NULL;

            hr = pPalette-&gt;GetColorCount(&amp;uiColorCount);

            if (SUCCEEDED(hr) &amp;&amp; (uiColorCount &gt; 0))
            {
                pColors = new WICColor[uiColorCount];

                if (pColors)
                {
                    hr = pPalette-&gt;GetColors(uiColorCount, pColors, &amp;uiActualColorCount);

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
        pPalette-&gt;Release();
    }

    if (pBitmapFrameDecode)
    {
        pBitmapFrameDecode-&gt;Release();
    }

    if (pDecoder)
    {
        pDecoder-&gt;Release();
    }

    if (pFactory)
    {
        pFactory-&gt;Release();
    }

    return hr;</pre>
</td>
</tr>
</table></span></div>
In this example code, <b>WICColor</b> is defined as a <b>UINT32</b> value with this layout: 

<pre class="syntax" xml:space="preserve"><code>0xAARRGGBB</code></pre>
The wincodec.h header type-defines <b>WICColor</b> as <b>UINT32</b>. 



