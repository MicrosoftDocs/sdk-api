---
UID: NF:d3d11_4.ID3D11VideoContext2.VideoProcessorGetOutputHDRMetaData
title: ID3D11VideoContext2::VideoProcessorGetOutputHDRMetaData (d3d11_4.h)
description: Gets the HDR metadata describing the display on which the content will be presented.
helpviewer_keywords: ["ID3D11VideoContext2 interface [Media Foundation]","VideoProcessorGetOutputHDRMetaData method","ID3D11VideoContext2.VideoProcessorGetOutputHDRMetaData","ID3D11VideoContext2::VideoProcessorGetOutputHDRMetaData","VideoProcessorGetOutputHDRMetaData","VideoProcessorGetOutputHDRMetaData method [Media Foundation]","VideoProcessorGetOutputHDRMetaData method [Media Foundation]","ID3D11VideoContext2 interface","d3d11_4/ID3D11VideoContext2::VideoProcessorGetOutputHDRMetaData","mf.id3d11videocontext2_videoprocessorgetoutputhdrmetadata"]
old-location: mf\id3d11videocontext2_videoprocessorgetoutputhdrmetadata.htm
tech.root: mf
ms.assetid: 5739668F-DCF8-448C-8690-E254315B92AF
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext2 interface [Media Foundation],VideoProcessorGetOutputHDRMetaData method, ID3D11VideoContext2.VideoProcessorGetOutputHDRMetaData, ID3D11VideoContext2::VideoProcessorGetOutputHDRMetaData, VideoProcessorGetOutputHDRMetaData, VideoProcessorGetOutputHDRMetaData method [Media Foundation], VideoProcessorGetOutputHDRMetaData method [Media Foundation],ID3D11VideoContext2 interface, d3d11_4/ID3D11VideoContext2::VideoProcessorGetOutputHDRMetaData, mf.id3d11videocontext2_videoprocessorgetoutputhdrmetadata
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
 - ID3D11VideoContext2::VideoProcessorGetOutputHDRMetaData
 - d3d11_4/ID3D11VideoContext2::VideoProcessorGetOutputHDRMetaData
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
 - ID3D11VideoContext2.VideoProcessorGetOutputHDRMetaData
---

# ID3D11VideoContext2::VideoProcessorGetOutputHDRMetaData


## -description

Gets the HDR metadata describing the display on which the content will be presented.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface.

### -param pType [out]

The type of HDR metadata supplied.

### -param Size [in]

The size of the memory referenced by <i>pHDRMetaData</i>.

If <i>pHDRMetaData</i> is NULL, <i>Size</i> should be 0.

### -param pMetaData [out]

Pointer to a buffer that receives the HDR metadata.

This parameter can be NULL.

## -remarks

This can be called multiple times, the first time to get the <i>Type</i> (in which case <i>Size</i> can be 0 and <i>pHDRMetaData</i> can be NULL) and then again to with non-NULL values to retrieve the actual metadata.

## -see-also

<a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11videocontext2">ID3D11VideoContext2</a>



<a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11videocontext2">ID3DVideoContext2</a>