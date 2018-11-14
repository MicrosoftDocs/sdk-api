---
UID: NF:wincodec.IWICMetadataQueryWriter.RemoveMetadataByName
title: IWICMetadataQueryWriter::RemoveMetadataByName
author: windows-sdk-content
description: Removes a metadata item from a specific location using a metadata query expression.
old-location: wic\_wic_codec_iwicmetadataquerywriter_removemetadatabyname.htm
tech.root: wic
ms.assetid: 419d56db-42a6-4467-8ec5-7c7d2c5cdcf4
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWICMetadataQueryWriter interface [Windows Imaging Component],RemoveMetadataByName method, IWICMetadataQueryWriter.RemoveMetadataByName, IWICMetadataQueryWriter::RemoveMetadataByName, RemoveMetadataByName, RemoveMetadataByName method [Windows Imaging Component], RemoveMetadataByName method [Windows Imaging Component],IWICMetadataQueryWriter interface, _wic_codec_iwicmetadataquerywriter_removemetadatabyname, wic._wic_codec_iwicmetadataquerywriter_removemetadatabyname, wincodec/IWICMetadataQueryWriter::RemoveMetadataByName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IWICMetadataQueryWriter.RemoveMetadataByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wincodec.h
: 
- IWICMetadataQueryWriter.RemoveMetadataByName
: 
---

# IWICMetadataQueryWriter::RemoveMetadataByName


## -description


Removes a metadata item from a specific location using a metadata query expression.


## -parameters




### -param wzName [in]

Type: <b>LPCWSTR</b>

The name of the metadata item to remove.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>RemoveMetadataByName</b> uses metadata query expressions to remove metadata. For more information on the metadata query language, see the <a href="https://msdn.microsoft.com/5ffa0a69-b53d-4be3-b802-deaaa743e6bd">Metadata Query Language Overview</a>.

If the metadata item is a metadata block, it is removed from the metadata hierarchy.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/a7cfaa6d-e17d-458a-ae63-72963615bef8">How-to: Re-encode a JPEG Image with Metadata</a>



<a href="https://msdn.microsoft.com/065cccc3-778f-42c4-823a-354b08bbd1f1">IWICMetadataQueryWriter</a>



<a href="https://msdn.microsoft.com/5ffa0a69-b53d-4be3-b802-deaaa743e6bd">Metadata Query Language Overview</a>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>
 

 

