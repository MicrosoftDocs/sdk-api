---
UID: NF:wincodecsdk.IWICMetadataWriterInfo.GetHeader
title: IWICMetadataWriterInfo::GetHeader (wincodecsdk.h)
description: Gets the metadata header for the metadata writer.
helpviewer_keywords: ["GetHeader","GetHeader method [Windows Imaging Component]","GetHeader method [Windows Imaging Component]","IWICMetadataWriterInfo interface","IWICMetadataWriterInfo interface [Windows Imaging Component]","GetHeader method","IWICMetadataWriterInfo.GetHeader","IWICMetadataWriterInfo::GetHeader","_wic_codec_iwicmetadatawriterinfo_getheader","wic._wic_codec_iwicmetadatawriterinfo_getheader","wincodecsdk/IWICMetadataWriterInfo::GetHeader"]
old-location: wic\_wic_codec_iwicmetadatawriterinfo_getheader.htm
tech.root: wic
ms.assetid: 156728ea-b4a3-47d7-b0d8-cd34881e9703
ms.date: 12/05/2018
ms.keywords: GetHeader, GetHeader method [Windows Imaging Component], GetHeader method [Windows Imaging Component],IWICMetadataWriterInfo interface, IWICMetadataWriterInfo interface [Windows Imaging Component],GetHeader method, IWICMetadataWriterInfo.GetHeader, IWICMetadataWriterInfo::GetHeader, _wic_codec_iwicmetadatawriterinfo_getheader, wic._wic_codec_iwicmetadatawriterinfo_getheader, wincodecsdk/IWICMetadataWriterInfo::GetHeader
req.header: wincodecsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodecsdk.idl
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
 - IWICMetadataWriterInfo::GetHeader
 - wincodecsdk/IWICMetadataWriterInfo::GetHeader
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
 - IWICMetadataWriterInfo.GetHeader
---

# IWICMetadataWriterInfo::GetHeader


## -description

Gets the metadata header for the metadata writer.

## -parameters

### -param guidContainerFormat [in]

Type: <b>REFGUID</b>

The format container GUID to obtain the header for.

### -param cbSize [in]

Type: <b>UINT</b>

The size of the <i>pHeader</i> buffer.

### -param pHeader [in, out]

Type: <b><a href="/windows/desktop/api/wincodecsdk/ns-wincodecsdk-wicmetadataheader">WICMetadataHeader</a>*</b>

Pointer that receives the <a href="/windows/desktop/api/wincodecsdk/ns-wincodecsdk-wicmetadataheader">WICMetadataHeader</a>.

### -param pcbActual [in, out]

Type: <b>UINT*</b>

The actual size of the header.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.