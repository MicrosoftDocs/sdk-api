---
UID: NF:wincodec.IWICImagingFactory.CreateFastMetadataEncoderFromFrameDecode
title: IWICImagingFactory::CreateFastMetadataEncoderFromFrameDecode (wincodec.h)
author: windows-sdk-content
description: Creates a new instance of the fast metadata encoder based on the given image frame.
old-location: wic\_wic_codec_iwicimagingfactory_createfastmetadataencoderfromframedecode.htm
tech.root: wic
ms.assetid: 076cfd22-f744-4152-a1c0-1e0f17ac764d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateFastMetadataEncoderFromFrameDecode, CreateFastMetadataEncoderFromFrameDecode method [Windows Imaging Component], CreateFastMetadataEncoderFromFrameDecode method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateFastMetadataEncoderFromFrameDecode method, IWICImagingFactory.CreateFastMetadataEncoderFromFrameDecode, IWICImagingFactory::CreateFastMetadataEncoderFromFrameDecode, _wic_codec_iwicimagingfactory_createfastmetadataencoderfromframedecode, wic._wic_codec_iwicimagingfactory_createfastmetadataencoderfromframedecode, wincodec/IWICImagingFactory::CreateFastMetadataEncoderFromFrameDecode
ms.topic: method
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
 - IWICImagingFactory.CreateFastMetadataEncoderFromFrameDecode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICImagingFactory::CreateFastMetadataEncoderFromFrameDecode


## -description


Creates a new instance of the fast metadata encoder based on the given image frame.


## -parameters




### -param pIFrameDecoder [in]

Type: <b><a href="https://msdn.microsoft.com/1498b800-6449-440f-bed7-85891637e559">IWICBitmapFrameDecode</a>*</b>

The <a href="https://msdn.microsoft.com/1498b800-6449-440f-bed7-85891637e559">IWICBitmapFrameDecode</a> to create the <a href="https://msdn.microsoft.com/c7b57a71-f1fe-4e30-a52e-72ab6ce021f7">IWICFastMetadataEncoder</a> from.


### -param ppIFastEncoder [out]

Type: <b><a href="https://msdn.microsoft.com/c7b57a71-f1fe-4e30-a52e-72ab6ce021f7">IWICFastMetadataEncoder</a>**</b>

When this method returns, contains a pointer to a new fast metadata encoder.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For a list of support metadata formats for fast metadata encoding, see <a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>.


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



<a href="https://msdn.microsoft.com/30d155b1-a46c-46c4-9f8f-fb56dc6bf0a9">IWICImagingFactory</a>



<a href="https://msdn.microsoft.com/5ffa0a69-b53d-4be3-b802-deaaa743e6bd">Metadata Query Language Overview</a>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee719653(v=VS.85).aspx">Writing Metadata</a>
 

 

