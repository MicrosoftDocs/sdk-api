---
UID: NN:wincodec.IWICFastMetadataEncoder
title: IWICFastMetadataEncoder (wincodec.h)
description: Exposes methods used for in-place metadata editing. A fast metadata encoder enables you to add and remove metadata to an image without having to fully re-encode the image.
helpviewer_keywords: ["IWICFastMetadataEncoder","IWICFastMetadataEncoder interface [Windows Imaging Component]","IWICFastMetadataEncoder interface [Windows Imaging Component]","described","_wic_codec_iwicfastmetadataencoder","wic._wic_codec_iwicfastmetadataencoder","wincodec/IWICFastMetadataEncoder"]
old-location: wic\_wic_codec_iwicfastmetadataencoder.htm
tech.root: wic
ms.assetid: c7b57a71-f1fe-4e30-a52e-72ab6ce021f7
ms.date: 12/05/2018
ms.keywords: IWICFastMetadataEncoder, IWICFastMetadataEncoder interface [Windows Imaging Component], IWICFastMetadataEncoder interface [Windows Imaging Component],described, _wic_codec_iwicfastmetadataencoder, wic._wic_codec_iwicfastmetadataencoder, wincodec/IWICFastMetadataEncoder
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
 - IWICFastMetadataEncoder
 - wincodec/IWICFastMetadataEncoder
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
 - IWICFastMetadataEncoder
---

# IWICFastMetadataEncoder interface


## -description

Exposes methods used for in-place metadata editing. A fast metadata encoder enables you to add and remove metadata to an image without having to fully re-encode the image.

## -inheritance

The <b>IWICFastMetadataEncoder</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICFastMetadataEncoder</b> also has these types of members:

## -remarks

A decoder must be created using the <a href="/windows/desktop/api/wincodec/ne-wincodec-wicdecodeoptions">WICDecodeOptions</a> value <b>WICDecodeMetadataCacheOnDemand</b> to perform in-place metadata updates. 
            Using the <b>WICDecodeMetadataCacheOnLoad</b> option causes the decoder to release the file stream necessary to perform the metadata updates. 
         

Not all metadata formats support fast metadata encoding. The native metadata handlers that support metadata are IFD, Exif, XMP, and GPS.
         

If a fast metadata encoder fails, the image will need to be fully re-encoded to add the metadata.
         


#### Examples

The following demonstrates how to obtain a fast metadata encoder from an image frame and use its query writer to write a metadata item.


```cpp
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
