---
UID: NF:wincodec.IWICMetadataQueryWriter.SetMetadataByName
title: IWICMetadataQueryWriter::SetMetadataByName (wincodec.h)
description: Sets a metadata item to a specific location.
helpviewer_keywords: ["IWICMetadataQueryWriter interface [Windows Imaging Component]","SetMetadataByName method","IWICMetadataQueryWriter.SetMetadataByName","IWICMetadataQueryWriter::SetMetadataByName","SetMetadataByName","SetMetadataByName method [Windows Imaging Component]","SetMetadataByName method [Windows Imaging Component]","IWICMetadataQueryWriter interface","_wic_codec_iwicmetadataquerywriter_setmetadatabyname","wic._wic_codec_iwicmetadataquerywriter_setmetadatabyname","wincodec/IWICMetadataQueryWriter::SetMetadataByName"]
old-location: wic\_wic_codec_iwicmetadataquerywriter_setmetadatabyname.htm
tech.root: wic
ms.assetid: fd3a9752-f13f-4f19-b2bd-04b5df1e0dd2
ms.date: 12/05/2018
ms.keywords: IWICMetadataQueryWriter interface [Windows Imaging Component],SetMetadataByName method, IWICMetadataQueryWriter.SetMetadataByName, IWICMetadataQueryWriter::SetMetadataByName, SetMetadataByName, SetMetadataByName method [Windows Imaging Component], SetMetadataByName method [Windows Imaging Component],IWICMetadataQueryWriter interface, _wic_codec_iwicmetadataquerywriter_setmetadatabyname, wic._wic_codec_iwicmetadataquerywriter_setmetadatabyname, wincodec/IWICMetadataQueryWriter::SetMetadataByName
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICMetadataQueryWriter::SetMetadataByName
 - wincodec/IWICMetadataQueryWriter::SetMetadataByName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICMetadataQueryWriter.SetMetadataByName
---

# IWICMetadataQueryWriter::SetMetadataByName


## -description

Sets a metadata item to a specific location.

## -parameters

### -param wzName [in]

Type: <b>LPCWSTR</b>

The name of the metadata item.

### -param pvarValue [in]

Type: <b>const <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

The metadata to set.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>SetMetadataByName</b> uses metadata query expressions to remove metadata. For more information on the metadata query language, see the <a href="/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>.

If the value set is a nested metadata block then use variant type <code>VT_UNKNOWN</code> and <i>pvarValue</i> pointing to the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataquerywriter">IWICMetadataQueryWriter</a> of the new metadata block.  
                The ordering of metadata items is at the discretion of the query writer since relative locations are not specified.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/wic/-wic-codec-jpegmetadataencoding">How-to: Re-encode a JPEG Image with Metadata</a>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataquerywriter">IWICMetadataQueryWriter</a>



<a href="/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>



<b>Other Resources</b>



<a href="/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>



<a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>