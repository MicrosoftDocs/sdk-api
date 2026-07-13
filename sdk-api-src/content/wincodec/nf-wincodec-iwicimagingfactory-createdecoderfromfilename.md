---
UID: NF:wincodec.IWICImagingFactory.CreateDecoderFromFilename
title: IWICImagingFactory::CreateDecoderFromFilename (wincodec.h)
description: Creates a new instance of the IWICBitmapDecoder class based on the given file.
helpviewer_keywords: ["CreateDecoderFromFilename","CreateDecoderFromFilename method [Windows Imaging Component]","CreateDecoderFromFilename method [Windows Imaging Component]","IWICImagingFactory interface","IWICImagingFactory interface [Windows Imaging Component]","CreateDecoderFromFilename method","IWICImagingFactory.CreateDecoderFromFilename","IWICImagingFactory::CreateDecoderFromFilename","_wic_codec_iwicimagingfactory_createdecoderfromfilename","wic._wic_codec_iwicimagingfactory_createdecoderfromfilename","wincodec/IWICImagingFactory::CreateDecoderFromFilename"]
old-location: wic\_wic_codec_iwicimagingfactory_createdecoderfromfilename.htm
tech.root: wic
ms.assetid: 100c54c7-bb10-47dd-8436-04282ec6b110
ms.date: 12/05/2018
ms.keywords: CreateDecoderFromFilename, CreateDecoderFromFilename method [Windows Imaging Component], CreateDecoderFromFilename method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateDecoderFromFilename method, IWICImagingFactory.CreateDecoderFromFilename, IWICImagingFactory::CreateDecoderFromFilename, _wic_codec_iwicimagingfactory_createdecoderfromfilename, wic._wic_codec_iwicimagingfactory_createdecoderfromfilename, wincodec/IWICImagingFactory::CreateDecoderFromFilename
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICImagingFactory::CreateDecoderFromFilename
 - wincodec/IWICImagingFactory::CreateDecoderFromFilename
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.lib
 - Windowscodecs.dll
api_name:
 - IWICImagingFactory.CreateDecoderFromFilename
---

# IWICImagingFactory::CreateDecoderFromFilename


## -description

Creates a new instance of the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder">IWICBitmapDecoder</a> class based on the given file.

## -parameters

### -param wzFilename [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated string that specifies the name of an object to create or open.

### -param pguidVendor [in]

Type: <b>const GUID*</b>

The GUID for the preferred decoder vendor. Use <b>NULL</b> if no preferred vendor.

### -param dwDesiredAccess [in]

Type: <b>DWORD</b>

The access to the object, which can be read, write, or both.
               

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>GENERIC_READ</dt>
</dl>
</td>
<td width="60%">
Read access.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>GENERIC_WRITE</dt>
</dl>
</td>
<td width="60%">
Write access.

</td>
</tr>
</table>
 

For more information, see <a href="/windows/desktop/SecAuthZ/generic-access-rights">Generic Access Rights</a>.

### -param metadataOptions [in]

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicdecodeoptions">WICDecodeOptions</a></b>

The <a href="/windows/desktop/api/wincodec/ne-wincodec-wicdecodeoptions">WICDecodeOptions</a> to use when creating the decoder.

### -param ppIDecoder [out, retval]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder">IWICBitmapDecoder</a>**</b>

A pointer that receives a pointer to the new <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder">IWICBitmapDecoder</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.