---
UID: NF:wincodecsdk.IWICMetadataBlockWriter.RemoveWriterByIndex
title: IWICMetadataBlockWriter::RemoveWriterByIndex method
author: windows-driver-content
description: Removes the metadata writer from the specified index location.
old-location: wic\_wic_codec_iwicmetadatablockwriter_removewriterbyindex.htm
old-project: wic
ms.assetid: 030c5b0e-5db7-40ae-889c-2e1335d2c50b
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IWICMetadataBlockWriter, IWICMetadataBlockWriter interface [Windows Imaging Component], RemoveWriterByIndex method, IWICMetadataBlockWriter::RemoveWriterByIndex, RemoveWriterByIndex method [Windows Imaging Component], RemoveWriterByIndex method [Windows Imaging Component], IWICMetadataBlockWriter interface, RemoveWriterByIndex,IWICMetadataBlockWriter.RemoveWriterByIndex, _wic_codec_iwicmetadatablockwriter_removewriterbyindex, wic._wic_codec_iwicmetadatablockwriter_removewriterbyindex, wincodecsdk/IWICMetadataBlockWriter::RemoveWriterByIndex
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
-	IWICMetadataBlockWriter.RemoveWriterByIndex
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICMetadataBlockWriter::RemoveWriterByIndex method


## -description


Removes the metadata writer from the specified index location.


## -parameters




### -param nIndex [in]

Type: <b>UINT</b>

The index of the metadata writer to remove.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 After removing a metadata writer, remaining metadata writers can be expected to move up to occupy the vacated location. Indexes for remaining metadata items as well as the count will change.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/58f03dc2-cc31-4d76-b75a-f332da1f900f">How to Write a WIC-Enabled CODEC</a>



<a href="https://msdn.microsoft.com/a7cfaa6d-e17d-458a-ae63-72963615bef8">How-to: Re-encode a JPEG Image with Metadata</a>



<a href="https://msdn.microsoft.com/d8e44c64-dd58-4d36-8add-0a0b2e2af5a4">IWICMetadataBlockWriter</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>
 

 

