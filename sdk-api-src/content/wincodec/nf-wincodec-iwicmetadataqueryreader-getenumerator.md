---
UID: NF:wincodec.IWICMetadataQueryReader.GetEnumerator
title: IWICMetadataQueryReader::GetEnumerator
author: windows-sdk-content
description: Gets an enumerator of all metadata items at the current relative location within the metadata hierarchy.
old-location: wic\_wic_codec_iwicmetadataqueryreader_getenumerator.htm
old-project: wic
ms.assetid: 8e9b0da5-90e3-4398-9113-0fb86a94cb0c
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetEnumerator, GetEnumerator method [Windows Imaging Component], GetEnumerator method [Windows Imaging Component],IWICMetadataQueryReader interface, IWICMetadataQueryReader interface [Windows Imaging Component],GetEnumerator method, IWICMetadataQueryReader.GetEnumerator, IWICMetadataQueryReader::GetEnumerator, _wic_codec_iwicmetadataqueryreader_getenumerator, wic._wic_codec_iwicmetadataqueryreader_getenumerator, wincodec/IWICMetadataQueryReader::GetEnumerator
ms.prod: windows
ms.technology: windows-sdk
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
-	IWICMetadataQueryReader.GetEnumerator
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICMetadataQueryReader::GetEnumerator


## -description


Gets an enumerator of all metadata items at the current relative location within the metadata hierarchy.


## -parameters




### -param ppIEnumString [out]

Type: <b><a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a>**</b>

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a> interface for the enumerator that contains query strings that can be used in the current <a href="https://msdn.microsoft.com/588e00d2-e166-4ce5-bd8a-50ad0d5a3db9">IWICMetadataQueryReader</a>.



## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The retrieved enumerator only contains query strings for the metadata blocks and items in the current level of the hierarchy.





## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/588e00d2-e166-4ce5-bd8a-50ad0d5a3db9">IWICMetadataQueryReader</a>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>
 

 

