---
UID: NF:wincodec.IWICBitmapEncoder.GetMetadataQueryWriter
title: IWICBitmapEncoder::GetMetadataQueryWriter (wincodec.h)
author: windows-sdk-content
description: Retrieves a metadata query writer for the encoder.
old-location: wic\_wic_codec_iwicbitmapencoder_getmetadataquerywriter.htm
tech.root: wic
ms.assetid: 11160c48-dbbe-45b6-864c-6a6713ec9ab5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetMetadataQueryWriter, GetMetadataQueryWriter method [Windows Imaging Component], GetMetadataQueryWriter method [Windows Imaging Component],IWICBitmapEncoder interface, IWICBitmapEncoder interface [Windows Imaging Component],GetMetadataQueryWriter method, IWICBitmapEncoder.GetMetadataQueryWriter, IWICBitmapEncoder::GetMetadataQueryWriter, _wic_codec_iwicbitmapencoder_getmetadataquerywriter, wic._wic_codec_iwicbitmapencoder_getmetadataquerywriter, wincodec/IWICBitmapEncoder::GetMetadataQueryWriter
ms.topic: method
f1_keywords: ["wincodec/IWICBitmapEncoder.GetMetadataQueryWriter"]
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
 - IWICBitmapEncoder.GetMetadataQueryWriter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICBitmapEncoder::GetMetadataQueryWriter


## -description


Retrieves a metadata query writer for the encoder.


## -parameters




### -param ppIMetadataQueryWriter [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataquerywriter">IWICMetadataQueryWriter</a>**</b>

When this method returns, contains a pointer to the encoder's metadata query writer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-codec-jpegmetadataencoding">How-to: Re-encode a JPEG Image with Metadata</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder">IWICBitmapEncoder</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>
 

 

