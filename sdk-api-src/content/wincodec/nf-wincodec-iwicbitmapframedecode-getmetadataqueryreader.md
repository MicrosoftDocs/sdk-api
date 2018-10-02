---
UID: NF:wincodec.IWICBitmapFrameDecode.GetMetadataQueryReader
title: IWICBitmapFrameDecode::GetMetadataQueryReader
author: windows-sdk-content
description: Retrieves a metadata query reader for the frame.
old-location: wic\_wic_codec_iwicbitmapframedecode_getmetadataqueryreader.htm
tech.root: wic
ms.assetid: e28de664-f9f1-4cf1-b2a7-f310548a3786
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetMetadataQueryReader, GetMetadataQueryReader method [Windows Imaging Component], GetMetadataQueryReader method [Windows Imaging Component],IWICBitmapFrameDecode interface, IWICBitmapFrameDecode interface [Windows Imaging Component],GetMetadataQueryReader method, IWICBitmapFrameDecode.GetMetadataQueryReader, IWICBitmapFrameDecode::GetMetadataQueryReader, _wic_codec_iwicbitmapframedecode_getmetadataqueryreader, wic._wic_codec_iwicbitmapframedecode_getmetadataqueryreader, wincodec/IWICBitmapFrameDecode::GetMetadataQueryReader
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWICBitmapFrameDecode.GetMetadataQueryReader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICBitmapFrameDecode::GetMetadataQueryReader


## -description


Retrieves a metadata query reader for the frame.


## -parameters




### -param ppIMetadataQueryReader [out]

Type: <b><a href="https://msdn.microsoft.com/588e00d2-e166-4ce5-bd8a-50ad0d5a3db9">IWICMetadataQueryReader</a>**</b>

When this method returns, contains a pointer to the frame's metadata query reader.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For image formats with one frame (JPG, PNG, JPEG-XR), the frame-level query reader of the first frame is used to access all image metadata, and the decoder-level query reader isn’t used. For formats with more than one frame (GIF, TIFF), the frame-level query reader for a given frame is used to access metadata specific to that frame, and in the case of GIF a decoder-level metadata reader will be present. If the decoder doesn’t support metadata (BMP, ICO), this will return <a href="https://msdn.microsoft.com/1ded909c-311b-49e3-ba23-b22cd7a77bc6">WINCODEC_ERR_UNSUPPORTEDOPERATION</a>.





## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/1498b800-6449-440f-bed7-85891637e559">IWICBitmapFrameDecode</a>



<a href="https://msdn.microsoft.com/5ffa0a69-b53d-4be3-b802-deaaa743e6bd">Metadata Query Language Overview</a>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>
 

 

