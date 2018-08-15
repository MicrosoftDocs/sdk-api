---
UID: NF:wincodecsdk.IWICMetadataBlockWriter.SetWriterByIndex
title: IWICMetadataBlockWriter::SetWriterByIndex
author: windows-sdk-content
description: Replaces the metadata writer at the specified index location.
old-location: wic\_wic_codec_iwicmetadatablockwriter_setwriterbyindex.htm
old-project: wic
ms.assetid: cf8f45ee-44ca-431c-b9c2-1b00c5574afe
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWICMetadataBlockWriter interface [Windows Imaging Component],SetWriterByIndex method, IWICMetadataBlockWriter.SetWriterByIndex, IWICMetadataBlockWriter::SetWriterByIndex, SetWriterByIndex, SetWriterByIndex method [Windows Imaging Component], SetWriterByIndex method [Windows Imaging Component],IWICMetadataBlockWriter interface, _wic_codec_iwicmetadatablockwriter_setwriterbyindex, wic._wic_codec_iwicmetadatablockwriter_setwriterbyindex, wincodecsdk/IWICMetadataBlockWriter::SetWriterByIndex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wincodecsdk.h
req.include-header: 
req.redist: 
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
 - IWICMetadataBlockWriter.SetWriterByIndex
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICMetadataBlockWriter::SetWriterByIndex


## -description


Replaces the metadata writer at the specified index location.


## -parameters




### -param nIndex [in]

Type: <b>UINT</b>

The index position at which to place the metadata writer. This index is zero-based.


### -param pIMetadataWriter [in]

Type: <b><a href="https://msdn.microsoft.com/7e742a96-f9d0-49e1-80e4-31ec90680e60">IWICMetadataWriter</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/7e742a96-f9d0-49e1-80e4-31ec90680e60">IWICMetadataWriter</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Typically, the current metadata writer at the specified index will be replaced with the new writer. However, the App0 metadata writer cannot be replaced within a JPEG stream. 

This function cannot be used to add metadata writers. If no metadata writer exists at the specified index, the function will fail.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/58f03dc2-cc31-4d76-b75a-f332da1f900f">How to Write a WIC-Enabled CODEC</a>



<a href="https://msdn.microsoft.com/a7cfaa6d-e17d-458a-ae63-72963615bef8">How-to: Re-encode a JPEG Image with Metadata</a>



<a href="https://msdn.microsoft.com/d8e44c64-dd58-4d36-8add-0a0b2e2af5a4">IWICMetadataBlockWriter</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>
 

 

