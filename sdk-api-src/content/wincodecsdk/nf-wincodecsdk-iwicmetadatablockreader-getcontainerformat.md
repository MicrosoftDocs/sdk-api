---
UID: NF:wincodecsdk.IWICMetadataBlockReader.GetContainerFormat
title: IWICMetadataBlockReader::GetContainerFormat
author: windows-driver-content
description: Retrieves the container format of the decoder.
old-location: wic\_wic_codec_iwicmetadatablockreader_getcontainerformat.htm
old-project: wic
ms.assetid: b53e6b4e-e5b9-4e4a-b10b-443e3ca2d689
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetContainerFormat, GetContainerFormat method [Windows Imaging Component], GetContainerFormat method [Windows Imaging Component],IWICMetadataBlockReader interface, IWICMetadataBlockReader interface [Windows Imaging Component],GetContainerFormat method, IWICMetadataBlockReader.GetContainerFormat, IWICMetadataBlockReader::GetContainerFormat, _wic_codec_iwicmetadatablockreader_getcontainerformat, wic._wic_codec_iwicmetadatablockreader_getcontainerformat, wincodecsdk/IWICMetadataBlockReader::GetContainerFormat
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
-	IWICMetadataBlockReader.GetContainerFormat
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICMetadataBlockReader::GetContainerFormat


## -description


Retrieves the container format of the decoder.


## -parameters




### -param pguidContainerFormat [out]

Type: <b>GUID*</b>

The container format of the decoder. The native container format GUIDs are listed in <a href="_wic_guids_clsids.htm">WIC GUIDs and CLSIDs</a>.


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
 

 

