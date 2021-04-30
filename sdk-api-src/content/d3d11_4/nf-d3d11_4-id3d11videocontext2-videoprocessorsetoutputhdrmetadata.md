---
UID: NF:d3d11_4.ID3D11VideoContext2.VideoProcessorSetOutputHDRMetaData
title: ID3D11VideoContext2::VideoProcessorSetOutputHDRMetaData (d3d11_4.h)
description: Sets the HDR metadata describing the display on which the content will be presented.
helpviewer_keywords: ["ID3D11VideoContext2 interface [Media Foundation]","VideoProcessorSetOutputHDRMetaData method","ID3D11VideoContext2.VideoProcessorSetOutputHDRMetaData","ID3D11VideoContext2::VideoProcessorSetOutputHDRMetaData","VideoProcessorSetOutputHDRMetaData","VideoProcessorSetOutputHDRMetaData method [Media Foundation]","VideoProcessorSetOutputHDRMetaData method [Media Foundation]","ID3D11VideoContext2 interface","d3d11_4/ID3D11VideoContext2::VideoProcessorSetOutputHDRMetaData","mf.id3d11videocontext2_videoprocessorsetoutputhdrmetadata"]
old-location: mf\id3d11videocontext2_videoprocessorsetoutputhdrmetadata.htm
tech.root: mf
ms.assetid: 5905E3F2-B0A3-4FF6-B498-BC24BFD3F58F
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext2 interface [Media Foundation],VideoProcessorSetOutputHDRMetaData method, ID3D11VideoContext2.VideoProcessorSetOutputHDRMetaData, ID3D11VideoContext2::VideoProcessorSetOutputHDRMetaData, VideoProcessorSetOutputHDRMetaData, VideoProcessorSetOutputHDRMetaData method [Media Foundation], VideoProcessorSetOutputHDRMetaData method [Media Foundation],ID3D11VideoContext2 interface, d3d11_4/ID3D11VideoContext2::VideoProcessorSetOutputHDRMetaData, mf.id3d11videocontext2_videoprocessorsetoutputhdrmetadata
req.header: d3d11_4.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11VideoContext2::VideoProcessorSetOutputHDRMetaData
 - d3d11_4/ID3D11VideoContext2::VideoProcessorSetOutputHDRMetaData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11_4.h
api_name:
 - ID3D11VideoContext2.VideoProcessorSetOutputHDRMetaData
---

# ID3D11VideoContext2::VideoProcessorSetOutputHDRMetaData


## -description

Sets the HDR metadata describing the display on which the content will be presented.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface.

### -param Type [in]

The type of HDR metadata supplied.

### -param Size [in]

The size of the HDR metadata supplied in <i>pHDRMetaData</i>.

For <b>DXGI_HDR_METADATA_TYPE_NONE</b>, the size should be 0.

For <b>DXGI_HDR_METADATA_TYPE_HDR10</b>, the size is <code>sizeof(DXGI_HDR_METADATA_HDR10)</code>.

### -param pHDRMetaData [in]

Pointer to the metadata information.

For <b>DXGI_HDR_METADATA_TYPE_NONE</b>, this should be NULL.

For <b>DXGI_HDR_METADATA_TYPE_HDR10</b>, this is a pointer to a <a href="/windows/desktop/api/dxgi1_5/ns-dxgi1_5-dxgi_hdr_metadata_hdr10">DXGI_HDR_METADATA_HDR10</a> structure.

## -remarks

When processing an HDR stream, the driver may use this metadata optimize the video for the output display.

## -see-also

<a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11videocontext2">ID3D11VideoContext2</a>



<a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11videocontext2">ID3DVideoContext2</a>