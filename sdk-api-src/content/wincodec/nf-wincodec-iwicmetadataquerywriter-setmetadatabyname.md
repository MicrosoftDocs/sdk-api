---
UID: NF:wincodec.IWICMetadataQueryWriter.SetMetadataByName
title: IWICMetadataQueryWriter::SetMetadataByName (wincodec.h)
author: windows-sdk-content
description: Sets a metadata item to a specific location.
old-location: wic\_wic_codec_iwicmetadataquerywriter_setmetadatabyname.htm
tech.root: wic
ms.assetid: fd3a9752-f13f-4f19-b2bd-04b5df1e0dd2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICMetadataQueryWriter interface [Windows Imaging Component],SetMetadataByName method, IWICMetadataQueryWriter.SetMetadataByName, IWICMetadataQueryWriter::SetMetadataByName, SetMetadataByName, SetMetadataByName method [Windows Imaging Component], SetMetadataByName method [Windows Imaging Component],IWICMetadataQueryWriter interface, _wic_codec_iwicmetadataquerywriter_setmetadatabyname, wic._wic_codec_iwicmetadataquerywriter_setmetadatabyname, wincodec/IWICMetadataQueryWriter::SetMetadataByName
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
 - IWICMetadataQueryWriter.SetMetadataByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICMetadataQueryWriter::SetMetadataByName


## -description


Sets a metadata item to a specific location.


## -parameters




### -param wzName [in]

Type: <b>LPCWSTR</b>

The name of the metadata item.


### -param pvarValue [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Aa380072(v=VS.85).aspx">PROPVARIANT</a>*</b>

The metadata to set.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>SetMetadataByName</b> uses metadata query expressions to remove metadata. For more information on the metadata query language, see the <a href="https://msdn.microsoft.com/5ffa0a69-b53d-4be3-b802-deaaa743e6bd">Metadata Query Language Overview</a>.

If the value set is a nested metadata block then use variant type <code>VT_UNKNOWN</code> and <i>pvarValue</i> pointing to the <a href="https://msdn.microsoft.com/065cccc3-778f-42c4-823a-354b08bbd1f1">IWICMetadataQueryWriter</a> of the new metadata block.  
                The ordering of metadata items is at the discretion of the query writer since relative locations are not specified.
            




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/a7cfaa6d-e17d-458a-ae63-72963615bef8">How-to: Re-encode a JPEG Image with Metadata</a>



<a href="https://msdn.microsoft.com/065cccc3-778f-42c4-823a-354b08bbd1f1">IWICMetadataQueryWriter</a>



<a href="https://msdn.microsoft.com/5ffa0a69-b53d-4be3-b802-deaaa743e6bd">Metadata Query Language Overview</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380072(v=VS.85).aspx">PROPVARIANT</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>
 

 

