---
UID: NF:wincodec.IWICMetadataQueryWriter.RemoveMetadataByName
title: IWICMetadataQueryWriter::RemoveMetadataByName (wincodec.h)
author: windows-sdk-content
description: Removes a metadata item from a specific location using a metadata query expression.
old-location: wic\_wic_codec_iwicmetadataquerywriter_removemetadatabyname.htm
tech.root: wic
ms.assetid: 419d56db-42a6-4467-8ec5-7c7d2c5cdcf4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICMetadataQueryWriter interface [Windows Imaging Component],RemoveMetadataByName method, IWICMetadataQueryWriter.RemoveMetadataByName, IWICMetadataQueryWriter::RemoveMetadataByName, RemoveMetadataByName, RemoveMetadataByName method [Windows Imaging Component], RemoveMetadataByName method [Windows Imaging Component],IWICMetadataQueryWriter interface, _wic_codec_iwicmetadataquerywriter_removemetadatabyname, wic._wic_codec_iwicmetadataquerywriter_removemetadatabyname, wincodec/IWICMetadataQueryWriter::RemoveMetadataByName
ms.topic: method
f1_keywords: 
 - "wincodec/IWICMetadataQueryWriter.RemoveMetadataByName"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



<b>RemoveMetadataByName</b> uses metadata query expressions to remove metadata. For more information on the metadata query language, see the <a href="https://docs.microsoft.com/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>.

If the metadata item is a metadata block, it is removed from the metadata hierarchy.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-codec-jpegmetadataencoding">How-to: Re-encode a JPEG Image with Metadata</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataquerywriter">IWICMetadataQueryWriter</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>
 

 

