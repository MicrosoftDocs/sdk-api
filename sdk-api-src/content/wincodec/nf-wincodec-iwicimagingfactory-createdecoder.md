---
UID: NF:wincodec.IWICImagingFactory.CreateDecoder
title: IWICImagingFactory::CreateDecoder (wincodec.h)
description: Creates a new instance of IWICBitmapDecoder.
helpviewer_keywords: ["CreateDecoder","CreateDecoder method [Windows Imaging Component]","CreateDecoder method [Windows Imaging Component]","IWICImagingFactory interface","IWICImagingFactory interface [Windows Imaging Component]","CreateDecoder method","IWICImagingFactory.CreateDecoder","IWICImagingFactory::CreateDecoder","_wic_codec_iwicimagingfactory_createdecoder","wic._wic_codec_iwicimagingfactory_createdecoder","wincodec/IWICImagingFactory::CreateDecoder"]
old-location: wic\_wic_codec_iwicimagingfactory_createdecoder.htm
tech.root: wic
ms.assetid: 0d0072ce-3480-4687-a4ea-640953cf5a36
ms.date: 12/05/2018
ms.keywords: CreateDecoder, CreateDecoder method [Windows Imaging Component], CreateDecoder method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateDecoder method, IWICImagingFactory.CreateDecoder, IWICImagingFactory::CreateDecoder, _wic_codec_iwicimagingfactory_createdecoder, wic._wic_codec_iwicimagingfactory_createdecoder, wincodec/IWICImagingFactory::CreateDecoder
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
 - IWICImagingFactory::CreateDecoder
 - wincodec/IWICImagingFactory::CreateDecoder
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
 - IWICImagingFactory.CreateDecoder
---

# IWICImagingFactory::CreateDecoder


## -description

Creates a new instance of <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder">IWICBitmapDecoder</a>.

## -parameters

### -param guidContainerFormat [in]

Type: <b>REFGUID</b>

The GUID for the desired container format.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>GUID_ContainerFormatBmp</dt>
</dl>
</td>
<td width="60%">
The BMP container format GUID.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>GUID_ContainerFormatPng</dt>
</dl>
</td>
<td width="60%">
The PNG container format GUID.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>GUID_ContainerFormatIco</dt>
</dl>
</td>
<td width="60%">
The ICO container format GUID.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>GUID_ContainerFormatJpeg</dt>
</dl>
</td>
<td width="60%">
The JPEG container format GUID.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>GUID_ContainerFormatTiff</dt>
</dl>
</td>
<td width="60%">
The TIFF container format GUID.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>GUID_ContainerFormatGif</dt>
</dl>
</td>
<td width="60%">
The GIF container format GUID.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>GUID_ContainerFormatWmp</dt>
</dl>
</td>
<td width="60%">
The HD Photo container format GUID.

</td>
</tr>
</table>

### -param pguidVendor [in]

Type: <b>const GUID*</b>

The GUID for the preferred encoder vendor. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>NULL</dt>
</dl>
</td>
<td width="60%">
No preferred codec vendor.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>GUID_VendorMicrosoft</dt>
</dl>
</td>
<td width="60%">
Prefer to use Microsoft encoder.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>GUID_VendorMicrosoftBuiltIn</dt>
</dl>
</td>
<td width="60%">
Prefer to use the native Microsoft encoder.

</td>
</tr>
</table>

### -param ppIDecoder [out, retval]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder">IWICBitmapDecoder</a>**</b>

A pointer that receives a pointer to a new <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder">IWICBitmapDecoder</a>. You must initialize this <b>IWICBitmapDecoder</b> on a stream using the <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-initialize">Initialize</a> method later.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Other values may be available for both <i>guidContainerFormat</i> and <i>pguidVendor</i> depending on the installed WIC-enabled encoders.
            The values listed are those that are natively supported by the operating system.

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory">IWICImagingFactory</a>



<a href="/windows/desktop/wic/-wic-guids-clsids">WIC GUIDs and CLSIDs</a>