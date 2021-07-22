---
UID: NF:wincodec.IWICImagingFactory.CreateBitmap
title: IWICImagingFactory::CreateBitmap (wincodec.h)
description: Creates an IWICBitmap object.
helpviewer_keywords: ["CreateBitmap","CreateBitmap method [Windows Imaging Component]","CreateBitmap method [Windows Imaging Component]","IWICImagingFactory interface","IWICImagingFactory interface [Windows Imaging Component]","CreateBitmap method","IWICImagingFactory.CreateBitmap","IWICImagingFactory::CreateBitmap","WICBitmapCacheOnDemand","WICBitmapCacheOnLoad","WICBitmapNoCache","_wic_codec_iwicimagingfactory_createbitmap","wic._wic_codec_iwicimagingfactory_createbitmap","wincodec/IWICImagingFactory::CreateBitmap"]
old-location: wic\_wic_codec_iwicimagingfactory_createbitmap.htm
tech.root: wic
ms.assetid: 76741d1e-3e1b-4018-b092-b668ecfd43c9
ms.date: 12/05/2018
ms.keywords: CreateBitmap, CreateBitmap method [Windows Imaging Component], CreateBitmap method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateBitmap method, IWICImagingFactory.CreateBitmap, IWICImagingFactory::CreateBitmap, WICBitmapCacheOnDemand, WICBitmapCacheOnLoad, WICBitmapNoCache, _wic_codec_iwicimagingfactory_createbitmap, wic._wic_codec_iwicimagingfactory_createbitmap, wincodec/IWICImagingFactory::CreateBitmap
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
 - IWICImagingFactory::CreateBitmap
 - wincodec/IWICImagingFactory::CreateBitmap
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
 - IWICImagingFactory.CreateBitmap
---

# IWICImagingFactory::CreateBitmap


## -description

Creates an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a> object.

## -parameters

### -param uiWidth [in]

Type: <b>UINT</b>

The width of the new bitmap .

### -param uiHeight [in]

Type: <b>UINT</b>

The height of the new bitmap.

### -param pixelFormat [in]

Type: <b>REFWICPixelFormatGUID</b>

The pixel format of the new bitmap.

### -param option [in]

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmapcreatecacheoption">WICBitmapCreateCacheOption</a></b>

The cache creation options of the new bitmap. This can be one of the values in the <a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmapcreatecacheoption">WICBitmapCreateCacheOption</a> enumeration.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WICBitmapCacheOnDemand"></a><a id="wicbitmapcacheondemand"></a><a id="WICBITMAPCACHEONDEMAND"></a><dl>
<dt><b>WICBitmapCacheOnDemand</b></dt>
</dl>
</td>
<td width="60%">
Allocates system memory for the bitmap at initialization.

</td>
</tr>
<tr>
<td width="40%"><a id="WICBitmapCacheOnLoad"></a><a id="wicbitmapcacheonload"></a><a id="WICBITMAPCACHEONLOAD"></a><dl>
<dt><b>WICBitmapCacheOnLoad</b></dt>
</dl>
</td>
<td width="60%">
Allocates system memory for the bitmap when the bitmap is first used.

</td>
</tr>
<tr>
<td width="40%"><a id="WICBitmapNoCache"></a><a id="wicbitmapnocache"></a><a id="WICBITMAPNOCACHE"></a><dl>
<dt><b>WICBitmapNoCache</b></dt>
</dl>
</td>
<td width="60%">
This option is not valid for this method and should not be used.

</td>
</tr>
</table>

### -param ppIBitmap [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a>**</b>

A pointer that receives a pointer to the new bitmap.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory">IWICImagingFactory</a>



<a href="/windows/desktop/wic/-wic-codec-native-pixel-formats">Native Pixel Formats</a>