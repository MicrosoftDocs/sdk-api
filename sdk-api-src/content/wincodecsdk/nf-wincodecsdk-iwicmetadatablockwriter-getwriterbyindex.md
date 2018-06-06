---
UID: NF:wincodecsdk.IWICMetadataBlockWriter.GetWriterByIndex
title: IWICMetadataBlockWriter::GetWriterByIndex
author: windows-sdk-content
description: Retrieves the IWICMetadataWriter that resides at the specified index.
old-location: wic\_wic_codec_iwicmetadatablockwriter_getwriterbyindex.htm
old-project: wic
ms.assetid: 14c8acb1-484a-46ad-8a38-79a4b1cfe0d1
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetWriterByIndex, GetWriterByIndex method [Windows Imaging Component], GetWriterByIndex method [Windows Imaging Component],IWICMetadataBlockWriter interface, IWICMetadataBlockWriter interface [Windows Imaging Component],GetWriterByIndex method, IWICMetadataBlockWriter.GetWriterByIndex, IWICMetadataBlockWriter::GetWriterByIndex, _wic_codec_iwicmetadatablockwriter_getwriterbyindex, wic._wic_codec_iwicmetadatablockwriter_getwriterbyindex, wincodecsdk/IWICMetadataBlockWriter::GetWriterByIndex
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WICPersistOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICMetadataBlockWriter.GetWriterByIndex
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICMetadataBlockWriter::GetWriterByIndex


## -description


Retrieves the <a href="https://msdn.microsoft.com/7e742a96-f9d0-49e1-80e4-31ec90680e60">IWICMetadataWriter</a> that resides at the specified index.


## -parameters




### -param nIndex [in]

Type: <b>UINT</b>

The index of the metadata writer to be retrieved. This index is zero-based.


### -param ppIMetadataWriter [out]

Type: <b><a href="https://msdn.microsoft.com/7e742a96-f9d0-49e1-80e4-31ec90680e60">IWICMetadataWriter</a>**</b>

When this method returns, contains a pointer to the metadata writer that resides at the specified index.


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
 

 

