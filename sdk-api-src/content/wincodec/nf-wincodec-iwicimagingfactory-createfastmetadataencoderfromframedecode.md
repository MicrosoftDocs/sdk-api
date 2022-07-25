---
UID: NF:wincodec.IWICImagingFactory.CreateFastMetadataEncoderFromFrameDecode
title: IWICImagingFactory::CreateFastMetadataEncoderFromFrameDecode (wincodec.h)
description: Creates a new instance of the fast metadata encoder based on the given image frame.
helpviewer_keywords: ["CreateFastMetadataEncoderFromFrameDecode","CreateFastMetadataEncoderFromFrameDecode method [Windows Imaging Component]","CreateFastMetadataEncoderFromFrameDecode method [Windows Imaging Component]","IWICImagingFactory interface","IWICImagingFactory interface [Windows Imaging Component]","CreateFastMetadataEncoderFromFrameDecode method","IWICImagingFactory.CreateFastMetadataEncoderFromFrameDecode","IWICImagingFactory::CreateFastMetadataEncoderFromFrameDecode","_wic_codec_iwicimagingfactory_createfastmetadataencoderfromframedecode","wic._wic_codec_iwicimagingfactory_createfastmetadataencoderfromframedecode","wincodec/IWICImagingFactory::CreateFastMetadataEncoderFromFrameDecode"]
old-location: wic\_wic_codec_iwicimagingfactory_createfastmetadataencoderfromframedecode.htm
tech.root: wic
ms.assetid: 076cfd22-f744-4152-a1c0-1e0f17ac764d
ms.date: 12/05/2018
ms.keywords: CreateFastMetadataEncoderFromFrameDecode, CreateFastMetadataEncoderFromFrameDecode method [Windows Imaging Component], CreateFastMetadataEncoderFromFrameDecode method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateFastMetadataEncoderFromFrameDecode method, IWICImagingFactory.CreateFastMetadataEncoderFromFrameDecode, IWICImagingFactory::CreateFastMetadataEncoderFromFrameDecode, _wic_codec_iwicimagingfactory_createfastmetadataencoderfromframedecode, wic._wic_codec_iwicimagingfactory_createfastmetadataencoderfromframedecode, wincodec/IWICImagingFactory::CreateFastMetadataEncoderFromFrameDecode
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
 - IWICImagingFactory::CreateFastMetadataEncoderFromFrameDecode
 - wincodec/IWICImagingFactory::CreateFastMetadataEncoderFromFrameDecode
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
 - IWICImagingFactory.CreateFastMetadataEncoderFromFrameDecode
---

# IWICImagingFactory::CreateFastMetadataEncoderFromFrameDecode


## -description

Creates a new instance of the fast metadata encoder based on the given image frame.

## -parameters

### -param pIFrameDecoder [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode">IWICBitmapFrameDecode</a>*</b>

The <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode">IWICBitmapFrameDecode</a> to create the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicfastmetadataencoder">IWICFastMetadataEncoder</a> from.

### -param ppIFastEncoder [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicfastmetadataencoder">IWICFastMetadataEncoder</a>**</b>

When this method returns, contains a pointer to a new fast metadata encoder.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For a list of support metadata formats for fast metadata encoding, see <a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>.


#### Examples

The following code demonstrates how to use the <b>CreateFastMetadataEncoderFromFrameDecode</b> method for fast metadata encoding.


```
IWICFastMetadataEncoder *pFME = NULL;
IWICMetadataQueryWriter *pFMEQW = NULL;

hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(pFrameDecode, &pFME);

if (SUCCEEDED(hr))
{
  hr = pFME->GetMetadataQueryWriter(&pFMEQW);
}

if (SUCCEEDED(hr))
{
  // Add additional metadata
  PROPVARIANT value;

  PropVariantInit(&value);

  value.vt = VT_UI2;
  value.uiVal = 99;
  hr = pFMEQW->SetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);

  PropVariantClear(&value);
}

if (SUCCEEDED(hr))
{
  hr = pFME->Commit();
}
```

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory">IWICImagingFactory</a>



<a href="/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>



<a href="/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>



<a href="/windows/desktop/wic/-wic-about-metadata">Writing Metadata</a>