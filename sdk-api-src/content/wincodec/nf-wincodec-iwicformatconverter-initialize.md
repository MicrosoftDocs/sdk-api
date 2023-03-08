---
UID: NF:wincodec.IWICFormatConverter.Initialize
title: IWICFormatConverter::Initialize (wincodec.h)
description: Initializes the format converter.
helpviewer_keywords: ["IWICFormatConverter interface [Windows Imaging Component]","Initialize method","IWICFormatConverter.Initialize","IWICFormatConverter::Initialize","Initialize","Initialize method [Windows Imaging Component]","Initialize method [Windows Imaging Component]","IWICFormatConverter interface","_wic_codec_iwicformatconverter_initialize","wic._wic_codec_iwicformatconverter_initialize","wincodec/IWICFormatConverter::Initialize"]
old-location: wic\_wic_codec_iwicformatconverter_initialize.htm
tech.root: wic
ms.assetid: ff046b2c-a863-48dd-9cbe-3c559c84b682
ms.author: windowssdkdev
ms.date: 3/9/2019
ms.keywords: IWICFormatConverter interface [Windows Imaging Component],Initialize method, IWICFormatConverter.Initialize, IWICFormatConverter::Initialize, Initialize, Initialize method [Windows Imaging Component], Initialize method [Windows Imaging Component],IWICFormatConverter interface, _wic_codec_iwicformatconverter_initialize, wic._wic_codec_iwicformatconverter_initialize, wincodec/IWICFormatConverter::Initialize
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
 - IWICFormatConverter::Initialize
 - wincodec/IWICFormatConverter::Initialize
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
 - IWICFormatConverter.Initialize
---

# IWICFormatConverter::Initialize


## -description

Initializes the format converter.

## -parameters

### -param pISource [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>*</b>

The input bitmap to convert

### -param dstFormat [in]

Type: <b>REFWICPixelFormatGUID</b>

The destination pixel format GUID.

### -param dither [in]

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmapdithertype">WICBitmapDitherType</a></b>

The <a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmapdithertype">WICBitmapDitherType</a> used for conversion.

### -param pIPalette [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicpalette">IWICPalette</a>*</b>

The palette to use for conversion.

### -param alphaThresholdPercent [in]

Type: <b>double</b>

The alpha threshold to use for conversion.

### -param paletteTranslate [in]

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmappalettetype">WICBitmapPaletteType</a></b>

The palette translation type to use for conversion.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If you do not have a predefined palette, you must first create one. Use <a href="/windows/win32/api/wincodec/nf-wincodec-iwicpalette-initializefrombitmap">InitializeFromBitmap</a> to create the palette object, then pass it in along with your other parameters.


<i>dither</i>, <i>pIPalette</i>, <i>alphaThresholdPercent</i>, and <i>paletteTranslate</i> are used to mitigate color loss when converting to a reduced bit-depth format. For conversions that do not need these settings, the following parameters values should be used: <i>dither</i> set to <b>WICBitmapDitherTypeNone</b>, <i>pIPalette</i> set to <b>NULL</b>, <i>alphaThresholdPercent</i> set to <b>0.0f</b>, and <i>paletteTranslate</i> set to <b>WICBitmapPaletteTypeCustom</b>.  


The basic algorithm involved when using an ordered dither requires a fixed palette, found in the <a href="/windows/win32/api/wincodec/ne-wincodec-wicbitmappalettetype">WICBitmapPaletteType</a> enumeration, in a specific order.

Often, the actual palette provided for the output may have a different ordering or some slight variation in the actual colors. This is the case when using the Microsoft Windows palette which has slight differences among versions of Windows.To provide for this, a palette and a palette translation are given to the format converter. The <i>pIPalette</i> is the actual destination palette to be used and the <i>paletteTranslate</i> is a fixed palette. Once the conversion is complete, the colors are mapped from the fixed palette to the actual colors in <i>pIPalette</i> using a nearest color matching algorithm.

 If colors in <i>pIPalette</i> do not closely match those in <i>paletteTranslate</i>, the mapping may produce undesirable results.

<b>WICBitmapDitherTypeOrdered4x4</b> can be useful in format conversions from 8-bit formats to 5- or 6-bit formats as there is no way to accurately convert color data.

<b>WICBitmapDitherTypeErrorDiffusion</b> selects the error diffusion algorithm and may be used with any palette. If an arbitrary palette is provided, <b>WICBitmapPaletteCustom</b> should be passed in as the <i>paletteTranslate</i>. Error diffusion often provides superior results compared to the ordered dithering algorithms especially when combined with the optimized palette generation functionality on the <a href="/windows/win32/api/wincodec/nn-wincodec-iwicpalette">IWICPalette</a>.

 When converting a bitmap which has an alpha channel, such as a Portable Network Graphics (PNG), to 8bpp, the alpha channel is normally ignored. Any pixels which were transparent in the original bitmap show up as black in the final output because both transparent and black have pixel values of zero in the respective formats.

Some 8bpp content can contains an alpha color; for instance, the Graphics Interchange Format (GIF) format allows for a single palette entry to be used as a transparent color.
For this type of content, <i>alphaThresholdPercent</i>  specifies what percentage of transparency should map to the transparent color. Because the alpha value is directly proportional to the opacity (not transparency) of a pixel, the <i>alphaThresholdPercent</i> indicates what level of opacity is mapped to the fully transparent color. 

For instance, 9.8% implies that any pixel with an alpha value of less than 25 will be mapped to the transparent color. A value of 100% maps all pixels which are not fully opaque to the transparent color. Note that the palette should provide a transparent color. If it does not, the 'transparent' color will be the one closest to zero - often black.

#### Examples

The following example converts an image frame to a 32bppPBGRA format with no dithering or alpha threshold. Direct2D requires bitmap sources to be in the a 32bppPBGRA format for rendering. For a full sample demonstrating the use of the <a href="/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter">IWICFormatConverter</a>, see the <a href="/windows/win32/wic/-wic-sample-d2d-viewer">WIC Image Viewer Using Direct2D Sample</a>.

```cpp
HRESULT hr = S_OK;

IWICBitmapDecoder *pIDecoder = NULL;
IWICBitmapFrameDecode *pIDecoderFrame  = NULL;
IWICFormatConverter *pIFormatConverter = NULL;

// Create the decoder.
hr = m_pIWICFactory->CreateDecoderFromFilename(
   L"turtle.jpg",                  // Image to be decoded
   NULL,                           // Do not prefer a particular vendor
   GENERIC_READ,                   // Desired read access to the file
   WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
   &pIDecoder                      // Pointer to the decoder
   );

// Retrieve the first bitmap frame.
if (SUCCEEDED(hr))
{
   hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
}


// Create the flip/rotator.
if (SUCCEEDED(hr))
{
   hr = m_pIWICFactory->CreateFormatConverter(&pIFormatConverter);
}

// Initialize the format converter.
if (SUCCEEDED(hr))
{
   hr = pIFormatConverter->Initialize(
       pIDecoderFrame,                  // Input source to convert
       GUID_WICPixelFormat32bppPBGRA,   // Destination pixel format
       WICBitmapDitherTypeNone,         // Specified dither pattern
       NULL,                            // Specify a particular palette 
       0.f,                             // Alpha threshold
       WICBitmapPaletteTypeCustom       // Palette translation type
       );
}
//Create render target and D2D bitmap from IWICBitmapSource
if (SUCCEEDED(hr))
{
   hr = CreateDeviceResources(hWnd);
}

if (SUCCEEDED(hr))
{
   // Need to release the previous D2DBitmap if there is one
   SafeRelease(&m_pD2DBitmap);
   hr = m_pRT->CreateBitmapFromWicBitmap(pIFormatConverter, NULL, &m_pD2DBitmap);
}

SafeRelease(&pIFormatConverter);
SafeRelease(&pIDecoderFrame);
SafeRelease(&pIDecoder);

```