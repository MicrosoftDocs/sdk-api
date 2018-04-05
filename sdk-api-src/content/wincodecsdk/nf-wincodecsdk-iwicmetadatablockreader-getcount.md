---
UID: NF:wincodecsdk.IWICMetadataBlockReader.GetCount
title: IWICMetadataBlockReader::GetCount method
author: windows-driver-content
description: Retrieves the number of top level metadata blocks.
old-location: wic\_wic_codec_iwicmetadatablockreader_getcount.htm
old-project: wic
ms.assetid: 212e2376-9fad-4bfc-8883-ce89d05c35e6
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: GetCount method [Windows Imaging Component], GetCount method [Windows Imaging Component], IWICMetadataBlockReader interface, GetCount,IWICMetadataBlockReader.GetCount, IWICMetadataBlockReader, IWICMetadataBlockReader interface [Windows Imaging Component], GetCount method, IWICMetadataBlockReader::GetCount, _wic_codec_iwicmetadatablockreader_getcount, wic._wic_codec_iwicmetadatablockreader_getcount, wincodecsdk/IWICMetadataBlockReader::GetCount
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
-	IWICMetadataBlockReader.GetCount
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICMetadataBlockReader::GetCount method


## -description


Retrieves the number of top level metadata blocks.


## -parameters




### -param pcCount [out]

Type: <b>UINT*</b>

When this method returns, contains the number of top level metadata blocks.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/58f03dc2-cc31-4d76-b75a-f332da1f900f">How to Write a WIC-Enabled CODEC</a>



<a href="https://msdn.microsoft.com/09614b44-ebc2-44f4-9755-9df62f1b2178">IWICMetadataBlockReader</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>



<a href="https://msdn.microsoft.com/a05b496a-bd4c-4065-8060-df0f8930cde7">Windows Imaging Component Overview</a>
 

 

