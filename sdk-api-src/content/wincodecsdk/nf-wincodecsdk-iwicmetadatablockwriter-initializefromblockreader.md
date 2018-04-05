---
UID: NF:wincodecsdk.IWICMetadataBlockWriter.InitializeFromBlockReader
title: IWICMetadataBlockWriter::InitializeFromBlockReader method
author: windows-driver-content
description: Initializes an IWICMetadataBlockWriter from the given IWICMetadataBlockReader. This will prepopulate the metadata block writer with all the metadata in the metadata block reader.
old-location: wic\_wic_codec_iwicmetadatablockwriter_initializefromblockreader.htm
old-project: wic
ms.assetid: 9ad9d818-7b3e-47eb-bc99-e26e7664383c
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: IWICMetadataBlockWriter, IWICMetadataBlockWriter interface [Windows Imaging Component], InitializeFromBlockReader method, IWICMetadataBlockWriter::InitializeFromBlockReader, InitializeFromBlockReader method [Windows Imaging Component], InitializeFromBlockReader method [Windows Imaging Component], IWICMetadataBlockWriter interface, InitializeFromBlockReader,IWICMetadataBlockWriter.InitializeFromBlockReader, _wic_codec_iwicmetadatablockwriter_initializefromblockreader, wic._wic_codec_iwicmetadatablockwriter_initializefromblockreader, wincodecsdk/IWICMetadataBlockWriter::InitializeFromBlockReader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodecsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodecsdk.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICPersistOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICMetadataBlockWriter.InitializeFromBlockReader
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICMetadataBlockWriter::InitializeFromBlockReader method


## -description


Initializes an <a href="https://msdn.microsoft.com/d8e44c64-dd58-4d36-8add-0a0b2e2af5a4">IWICMetadataBlockWriter</a> from the given <a href="https://msdn.microsoft.com/09614b44-ebc2-44f4-9755-9df62f1b2178">IWICMetadataBlockReader</a>. This will prepopulate the metadata block writer with all the metadata in the metadata block reader.


## -parameters




### -param pIMDBlockReader [in]

Type: <b><a href="https://msdn.microsoft.com/09614b44-ebc2-44f4-9755-9df62f1b2178">IWICMetadataBlockReader</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/09614b44-ebc2-44f4-9755-9df62f1b2178">IWICMetadataBlockReader</a> used to initialize the block writer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/58f03dc2-cc31-4d76-b75a-f332da1f900f">How to Write a WIC-Enabled CODEC</a>



<a href="https://msdn.microsoft.com/a7cfaa6d-e17d-458a-ae63-72963615bef8">How-to: Re-encode a JPEG Image with Metadata</a>



<a href="https://msdn.microsoft.com/d8e44c64-dd58-4d36-8add-0a0b2e2af5a4">IWICMetadataBlockWriter</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>
 

 

