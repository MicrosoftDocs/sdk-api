---
UID: NF:wincodec.IWICFastMetadataEncoder.GetMetadataQueryWriter
title: IWICFastMetadataEncoder::GetMetadataQueryWriter
author: windows-driver-content
description: Retrieves a metadata query writer for fast metadata encoding.
old-location: wic\_wic_codec_iwicfastmetadataencoder_getmetadataquerywriter.htm
old-project: wic
ms.assetid: 1d8a0993-101a-4aa5-9e2f-c3f95b9d3d3f
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetMetadataQueryWriter, GetMetadataQueryWriter method [Windows Imaging Component], GetMetadataQueryWriter method [Windows Imaging Component],IWICFastMetadataEncoder interface, IWICFastMetadataEncoder interface [Windows Imaging Component],GetMetadataQueryWriter method, IWICFastMetadataEncoder.GetMetadataQueryWriter, IWICFastMetadataEncoder::GetMetadataQueryWriter, _wic_codec_iwicfastmetadataencoder_getmetadataquerywriter, wic._wic_codec_iwicfastmetadataencoder_getmetadataquerywriter, wincodec/IWICFastMetadataEncoder::GetMetadataQueryWriter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICFastMetadataEncoder.GetMetadataQueryWriter
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICFastMetadataEncoder::GetMetadataQueryWriter


## -description


Retrieves a metadata query writer for fast metadata encoding.


## -parameters




### -param ppIMetadataQueryWriter [out]

Type: <b><a href="https://msdn.microsoft.com/065cccc3-778f-42c4-823a-354b08bbd1f1">IWICMetadataQueryWriter</a>**</b>

When this method returns, contains a pointer to the fast metadata encoder's metadata query writer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/c7b57a71-f1fe-4e30-a52e-72ab6ce021f7">IWICFastMetadataEncoder</a>



<a href="https://msdn.microsoft.com/5ffa0a69-b53d-4be3-b802-deaaa743e6bd">Metadata Query Language Overview</a>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>
 

 

