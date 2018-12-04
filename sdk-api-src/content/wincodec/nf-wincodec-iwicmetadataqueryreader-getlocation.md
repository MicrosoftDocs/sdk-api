---
UID: NF:wincodec.IWICMetadataQueryReader.GetLocation
title: IWICMetadataQueryReader::GetLocation
author: windows-sdk-content
description: Retrieves the current path relative to the root metadata block.
old-location: wic\_wic_codec_iwicmetadataqueryreader_getlocation.htm
tech.root: wic
ms.assetid: e63fad36-e0b7-46b3-a854-d59cfcf20728
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetLocation, GetLocation method [Windows Imaging Component], GetLocation method [Windows Imaging Component],IWICMetadataQueryReader interface, IWICMetadataQueryReader interface [Windows Imaging Component],GetLocation method, IWICMetadataQueryReader.GetLocation, IWICMetadataQueryReader::GetLocation, _wic_codec_iwicmetadataqueryreader_getlocation, wic._wic_codec_iwicmetadataqueryreader_getlocation, wincodec/IWICMetadataQueryReader::GetLocation
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
 - IWICMetadataQueryReader.GetLocation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICMetadataQueryReader::GetLocation


## -description


Retrieves the current path relative to the root metadata block.


## -parameters




### -param cchMaxLength [in]

Type: <b>UINT</b>

The length of the <i>wzNamespace</i> buffer.


### -param wzNamespace [in, out]

Type: <b>WCHAR*</b>

Pointer that receives the current namespace location.


### -param pcchActualLength [out]

Type: <b>UINT*</b>

The actual buffer length that was needed to retrieve the current namespace location.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If you pass <b>NULL</b> to <i>wzNamespace</i>, <b>GetLocation</b> ignores <i>cchMaxLength</i> and returns the required buffer length to store the path in the variable that <i>pcchActualLength</i> points to.


If the query reader is relative to the top of the metadata hierarchy, it will return a single-char string.

If the query reader is relative to a nested metadata block, this method will return the path to the current query reader.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/588e00d2-e166-4ce5-bd8a-50ad0d5a3db9">IWICMetadataQueryReader</a>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>
 

 

