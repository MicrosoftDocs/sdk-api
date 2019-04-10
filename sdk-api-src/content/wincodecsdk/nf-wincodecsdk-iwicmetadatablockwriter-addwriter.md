---
UID: NF:wincodecsdk.IWICMetadataBlockWriter.AddWriter
title: IWICMetadataBlockWriter::AddWriter (wincodecsdk.h)
author: windows-sdk-content
description: Adds a top-level metadata block by adding a IWICMetadataWriter for it.
old-location: wic\_wic_codec_iwicmetadatablockwriter_addwriter.htm
tech.root: wic
ms.assetid: 25a0e662-a249-4218-a77e-37b11e0f8536
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddWriter, AddWriter method [Windows Imaging Component], AddWriter method [Windows Imaging Component],IWICMetadataBlockWriter interface, IWICMetadataBlockWriter interface [Windows Imaging Component],AddWriter method, IWICMetadataBlockWriter.AddWriter, IWICMetadataBlockWriter::AddWriter, _wic_codec_iwicmetadatablockwriter_addwriter, wic._wic_codec_iwicmetadatablockwriter_addwriter, wincodecsdk/IWICMetadataBlockWriter::AddWriter
ms.topic: method
req.header: wincodecsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodecsdk.idl
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
 - IWICMetadataBlockWriter.AddWriter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICMetadataBlockWriter::AddWriter


## -description


Adds a top-level metadata block by adding a <a href="https://msdn.microsoft.com/7e742a96-f9d0-49e1-80e4-31ec90680e60">IWICMetadataWriter</a> for it.


## -parameters




### -param pIMetadataWriter [in]

Type: <b><a href="https://msdn.microsoft.com/7e742a96-f9d0-49e1-80e4-31ec90680e60">IWICMetadataWriter</a>*</b>

A pointer to the metadata writer to add to the image.


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
 

 

