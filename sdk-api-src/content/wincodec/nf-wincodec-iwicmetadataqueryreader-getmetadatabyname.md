---
UID: NF:wincodec.IWICMetadataQueryReader.GetMetadataByName
title: IWICMetadataQueryReader::GetMetadataByName
author: windows-sdk-content
description: Retrieves the metadata block or item identified by a metadata query expression.
old-location: wic\_wic_codec_iwicmetadataqueryreader_getmetadatabyname.htm
tech.root: wic
ms.assetid: 29d53a14-0509-4a96-9b8b-59952770559a
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetMetadataByName, GetMetadataByName method [Windows Imaging Component], GetMetadataByName method [Windows Imaging Component],IWICMetadataQueryReader interface, IWICMetadataQueryReader interface [Windows Imaging Component],GetMetadataByName method, IWICMetadataQueryReader.GetMetadataByName, IWICMetadataQueryReader::GetMetadataByName, _wic_codec_iwicmetadataqueryreader_getmetadatabyname, wic._wic_codec_iwicmetadataqueryreader_getmetadatabyname, wincodec/IWICMetadataQueryReader::GetMetadataByName
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
 - IWICMetadataQueryReader.GetMetadataByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICMetadataQueryReader::GetMetadataByName


## -description


Retrieves the metadata block or item identified by a metadata query expression. 


## -parameters




### -param wzName [in]

Type: <b>LPCWSTR</b>

The query expression to the requested metadata block or item.


### -param pvarValue [in, out]

Type: <b><a href="_stg_propvariant">PROPVARIANT</a>*</b>

When this method returns, contains the metadata block or item requested.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>GetMetadataByName</b> uses metadata query expressions to access embedded metadata. For more information on the metadata query language, see the <a href="https://msdn.microsoft.com/5ffa0a69-b53d-4be3-b802-deaaa743e6bd">Metadata Query Language Overview</a>.

If multiple blocks or items exist that are expressed by the same query expression, the first metadata block or item found will be returned.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/588e00d2-e166-4ce5-bd8a-50ad0d5a3db9">IWICMetadataQueryReader</a>



<a href="https://msdn.microsoft.com/5ffa0a69-b53d-4be3-b802-deaaa743e6bd">Metadata Query Language Overview</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="_stg_propvariant">PROPVARIANT</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>
 

 

