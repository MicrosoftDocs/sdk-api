---
UID: NF:wincodec.IWICBitmapDecoder.GetMetadataQueryReader
title: IWICBitmapDecoder::GetMetadataQueryReader
author: windows-sdk-content
description: Retrieves the metadata query reader from the decoder.
old-location: wic\_wic_codec_iwicbitmapdecoder_getmetadataqueryreader.htm
old-project: wic
ms.assetid: 353ce6d8-ef33-44b6-ab8a-7c5903a024f6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetMetadataQueryReader, GetMetadataQueryReader method [Windows Imaging Component], GetMetadataQueryReader method [Windows Imaging Component],IWICBitmapDecoder interface, IWICBitmapDecoder interface [Windows Imaging Component],GetMetadataQueryReader method, IWICBitmapDecoder.GetMetadataQueryReader, IWICBitmapDecoder::GetMetadataQueryReader, _wic_codec_iwicbitmapdecoder_getmetadataqueryreader, wic._wic_codec_iwicbitmapdecoder_getmetadataqueryreader, wincodec/IWICBitmapDecoder::GetMetadataQueryReader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.redist: 
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
 - IWICBitmapDecoder.GetMetadataQueryReader
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapDecoder::GetMetadataQueryReader


## -description


Retrieves the metadata query reader from the decoder.


## -parameters




### -param ppIMetadataQueryReader [out]

Type: <b><a href="https://msdn.microsoft.com/588e00d2-e166-4ce5-bd8a-50ad0d5a3db9">IWICMetadataQueryReader</a>**</b>

Receives a pointer to the decoder's <a href="https://msdn.microsoft.com/588e00d2-e166-4ce5-bd8a-50ad0d5a3db9">IWICMetadataQueryReader</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If an image format does not support container-level metadata, this will return <a href="https://msdn.microsoft.com/1ded909c-311b-49e3-ba23-b22cd7a77bc6">WINCODEC_ERR_UNSUPPORTEDOPERATION</a>. The only Windows provided image format that supports container-level metadata is GIF. Instead, use <a href="https://msdn.microsoft.com/e28de664-f9f1-4cf1-b2a7-f310548a3786">IWICBitmapFrameDecode::GetMetadataQueryReader</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a>



<a href="https://msdn.microsoft.com/5ffa0a69-b53d-4be3-b802-deaaa743e6bd">Metadata Query Language Overview</a>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>
 

 

