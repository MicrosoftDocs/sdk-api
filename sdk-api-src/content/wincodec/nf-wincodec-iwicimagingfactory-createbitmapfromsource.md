---
UID: NF:wincodec.IWICImagingFactory.CreateBitmapFromSource
title: IWICImagingFactory::CreateBitmapFromSource (wincodec.h)
description: Creates a IWICBitmap from a IWICBitmapSource.
helpviewer_keywords: ["CreateBitmapFromSource","CreateBitmapFromSource method [Windows Imaging Component]","CreateBitmapFromSource method [Windows Imaging Component]","IWICImagingFactory interface","IWICImagingFactory interface [Windows Imaging Component]","CreateBitmapFromSource method","IWICImagingFactory.CreateBitmapFromSource","IWICImagingFactory::CreateBitmapFromSource","WICBitmapCacheOnDemand","WICBitmapCacheOnLoad","WICBitmapNoCache","_wic_codec_iwicimagingfactory_createbitmapfromsource","wic._wic_codec_iwicimagingfactory_createbitmapfromsource","wincodec/IWICImagingFactory::CreateBitmapFromSource"]
old-location: wic\_wic_codec_iwicimagingfactory_createbitmapfromsource.htm
tech.root: wic
ms.assetid: b3b9057f-e39a-4e7b-a3dc-0942d55c25e0
ms.date: 12/05/2018
ms.keywords: CreateBitmapFromSource, CreateBitmapFromSource method [Windows Imaging Component], CreateBitmapFromSource method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateBitmapFromSource method, IWICImagingFactory.CreateBitmapFromSource, IWICImagingFactory::CreateBitmapFromSource, WICBitmapCacheOnDemand, WICBitmapCacheOnLoad, WICBitmapNoCache, _wic_codec_iwicimagingfactory_createbitmapfromsource, wic._wic_codec_iwicimagingfactory_createbitmapfromsource, wincodec/IWICImagingFactory::CreateBitmapFromSource
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
 - IWICImagingFactory::CreateBitmapFromSource
 - wincodec/IWICImagingFactory::CreateBitmapFromSource
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
 - IWICImagingFactory.CreateBitmapFromSource
---

# IWICImagingFactory::CreateBitmapFromSource


## -description

Creates a <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a> from a <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>.

## -parameters

### -param pIBitmapSource [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>*</b>

The <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a> to create the bitmap from.

### -param option [in]

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmapcreatecacheoption">WICBitmapCreateCacheOption</a></b>

The cache options of the new bitmap.  This can be one of the values in the <a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmapcreatecacheoption">WICBitmapCreateCacheOption</a> enumeration.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WICBitmapNoCache"></a><a id="wicbitmapnocache"></a><a id="WICBITMAPNOCACHE"></a><dl>
<dt><b>WICBitmapNoCache</b></dt>
</dl>
</td>
<td width="60%">
Do not create a system memory copy. Share the bitmap with the source.


</td>
</tr>
<tr>
<td width="40%"><a id="WICBitmapCacheOnDemand"></a><a id="wicbitmapcacheondemand"></a><a id="WICBITMAPCACHEONDEMAND"></a><dl>
<dt><b>WICBitmapCacheOnDemand</b></dt>
</dl>
</td>
<td width="60%">
Create a system memory copy when the bitmap is first used.


</td>
</tr>
<tr>
<td width="40%"><a id="WICBitmapCacheOnLoad"></a><a id="wicbitmapcacheonload"></a><a id="WICBITMAPCACHEONLOAD"></a><dl>
<dt><b>WICBitmapCacheOnLoad</b></dt>
</dl>
</td>
<td width="60%">
Create a system memory copy when this method is called.


</td>
</tr>
</table>

### -param ppIBitmap [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a>**</b>

A pointer that receives a pointer to the new bitmap.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.