---
UID: NF:wincodec.IWICBitmapSource.CopyPalette
title: IWICBitmapSource::CopyPalette (wincodec.h)
description: Retrieves the color table for indexed pixel formats.
helpviewer_keywords: ["CopyPalette","CopyPalette method [Windows Imaging Component]","CopyPalette method [Windows Imaging Component]","IWICBitmapSource interface","IWICBitmapSource interface [Windows Imaging Component]","CopyPalette method","IWICBitmapSource.CopyPalette","IWICBitmapSource::CopyPalette","_wic_codec_iwicbitmapsource_copypalette","wic._wic_codec_iwicbitmapsource_copypalette","wincodec/IWICBitmapSource::CopyPalette"]
old-location: wic\_wic_codec_iwicbitmapsource_copypalette.htm
tech.root: wic
ms.assetid: 5e45ca4a-2d14-4829-9542-9cfc3e4b0d73
ms.date: 12/05/2018
ms.keywords: CopyPalette, CopyPalette method [Windows Imaging Component], CopyPalette method [Windows Imaging Component],IWICBitmapSource interface, IWICBitmapSource interface [Windows Imaging Component],CopyPalette method, IWICBitmapSource.CopyPalette, IWICBitmapSource::CopyPalette, _wic_codec_iwicbitmapsource_copypalette, wic._wic_codec_iwicbitmapsource_copypalette, wincodec/IWICBitmapSource::CopyPalette
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
 - IWICBitmapSource::CopyPalette
 - wincodec/IWICBitmapSource::CopyPalette
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
 - IWICBitmapSource.CopyPalette
---

# IWICBitmapSource::CopyPalette


## -description

Retrieves the color table for indexed pixel formats.

## -parameters

### -param pIPalette [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicpalette">IWICPalette</a>*</b>

An <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicpalette">IWICPalette</a>. A palette can be created using the <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createpalette">CreatePalette</a> method.

## -returns

Type: <b>HRESULT</b>

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINCODEC_ERR_PALETTEUNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The palette was unavailable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The palette was successfully copied.

</td>
</tr>
</table>

## -remarks

If the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a> is an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode">IWICBitmapFrameDecode</a>, the function may return the image's global palette if a frame-level palette is not available.
            The global palette may also be retrieved using the <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-copypalette">CopyPalette</a> method.