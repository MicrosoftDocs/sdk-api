---
UID: NF:wincodec.IWICImagingFactory.CreateFastMetadataEncoderFromDecoder
title: IWICImagingFactory::CreateFastMetadataEncoderFromDecoder
author: windows-sdk-content
description: Creates a new instance of the fast metadata encoder based on the given IWICBitmapDecoder.
old-location: wic\_wic_codec_iwicimagingfactory_createfastmetadataencoderfromdecoder.htm
old-project: wic
ms.assetid: 3264a987-4308-4c50-b99c-70142bc49476
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateFastMetadataEncoderFromDecoder, CreateFastMetadataEncoderFromDecoder method [Windows Imaging Component], CreateFastMetadataEncoderFromDecoder method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateFastMetadataEncoderFromDecoder method, IWICImagingFactory.CreateFastMetadataEncoderFromDecoder, IWICImagingFactory::CreateFastMetadataEncoderFromDecoder, _wic_codec_iwicimagingfactory_createfastmetadataencoderfromdecoder, wic._wic_codec_iwicimagingfactory_createfastmetadataencoderfromdecoder, wincodec/IWICImagingFactory::CreateFastMetadataEncoderFromDecoder
ms.prod: windows
ms.technology: windows-sdk
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
 - IWICImagingFactory.CreateFastMetadataEncoderFromDecoder
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICImagingFactory::CreateFastMetadataEncoderFromDecoder


## -description


Creates a new instance of the fast metadata encoder based on the given <a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a>.


## -parameters




### -param pIDecoder [in]

Type: <b><a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a>*</b>

The decoder to create the fast metadata encoder from.


### -param ppIFastEncoder [out]

Type: <b><a href="https://msdn.microsoft.com/c7b57a71-f1fe-4e30-a52e-72ab6ce021f7">IWICFastMetadataEncoder</a>**</b>

When this method returns, contains a pointer to the new <a href="https://msdn.microsoft.com/c7b57a71-f1fe-4e30-a52e-72ab6ce021f7">IWICFastMetadataEncoder</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The Windows provided codecs do not support fast metadata encoding at the decoder level, and only support fast metadata encoding at the frame level. To create a fast metadata encoder from a frame, see <a href="https://msdn.microsoft.com/076cfd22-f744-4152-a1c0-1e0f17ac764d">CreateFastMetadataEncoderFromFrameDecode</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/30d155b1-a46c-46c4-9f8f-fb56dc6bf0a9">IWICImagingFactory</a>



<a href="https://msdn.microsoft.com/5ffa0a69-b53d-4be3-b802-deaaa743e6bd">Metadata Query Language Overview</a>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>
 

 

