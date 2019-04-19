---
UID: NF:wincodec.IWICMetadataQueryReader.GetContainerFormat
title: IWICMetadataQueryReader::GetContainerFormat (wincodec.h)
author: windows-sdk-content
description: Gets the metadata query readers container format.
old-location: wic\_wic_codec_iwicmetadataqueryreader_getcontainerformat.htm
tech.root: wic
ms.assetid: f27c576a-3ff8-42bd-bad9-f7df18351a7f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetContainerFormat, GetContainerFormat method [Windows Imaging Component], GetContainerFormat method [Windows Imaging Component],IWICMetadataQueryReader interface, IWICMetadataQueryReader interface [Windows Imaging Component],GetContainerFormat method, IWICMetadataQueryReader.GetContainerFormat, IWICMetadataQueryReader::GetContainerFormat, _wic_codec_iwicmetadataqueryreader_getcontainerformat, wic._wic_codec_iwicmetadataqueryreader_getcontainerformat, wincodec/IWICMetadataQueryReader::GetContainerFormat
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
 - IWICMetadataQueryReader.GetContainerFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICMetadataQueryReader::GetContainerFormat


## -description


Gets the metadata query readers container format.


## -parameters




### -param pguidContainerFormat [out]

Type: <b>GUID*</b>

Pointer that receives the cointainer format GUID.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/588e00d2-e166-4ce5-bd8a-50ad0d5a3db9">IWICMetadataQueryReader</a>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>
 

 

