---
UID: NF:d3d11_1.ID3D11VideoContext1.VideoProcessorGetStreamMirror
title: ID3D11VideoContext1::VideoProcessorGetStreamMirror (d3d11_1.h)
description: Gets values that indicate whether the video processor input stream is being flipped vertically or horizontally.
helpviewer_keywords: ["ID3D11VideoContext1 interface [Media Foundation]","VideoProcessorGetStreamMirror method","ID3D11VideoContext1.VideoProcessorGetStreamMirror","ID3D11VideoContext1::VideoProcessorGetStreamMirror","VideoProcessorGetStreamMirror","VideoProcessorGetStreamMirror method [Media Foundation]","VideoProcessorGetStreamMirror method [Media Foundation]","ID3D11VideoContext1 interface","d3d11_1/ID3D11VideoContext1::VideoProcessorGetStreamMirror","mf.id3d11videocontext1_videoprocessorgetstreammirror"]
old-location: mf\id3d11videocontext1_videoprocessorgetstreammirror.htm
tech.root: mf
ms.assetid: DAB96601-C1B5-4B23-BD88-0C5CB515E842
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext1 interface [Media Foundation],VideoProcessorGetStreamMirror method, ID3D11VideoContext1.VideoProcessorGetStreamMirror, ID3D11VideoContext1::VideoProcessorGetStreamMirror, VideoProcessorGetStreamMirror, VideoProcessorGetStreamMirror method [Media Foundation], VideoProcessorGetStreamMirror method [Media Foundation],ID3D11VideoContext1 interface, d3d11_1/ID3D11VideoContext1::VideoProcessorGetStreamMirror, mf.id3d11videocontext1_videoprocessorgetstreammirror
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - ID3D11VideoContext1::VideoProcessorGetStreamMirror
 - d3d11_1/ID3D11VideoContext1::VideoProcessorGetStreamMirror
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11_1.h
api_name:
 - ID3D11VideoContext1.VideoProcessorGetStreamMirror
---

# ID3D11VideoContext1::VideoProcessorGetStreamMirror


## -description

Gets values that indicate whether the video processor input stream is  being flipped vertically or horizontally.

## -parameters

### -param pVideoProcessor [in]

Type: <b>ID3D11VideoProcessor*</b>

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface.

### -param StreamIndex [in]

Type: <b>UINT</b>

An index identifying the input stream.

### -param pEnable [out]

Type: <b>BOOL*</b>

A pointer to a boolean value indicating whether mirroring is enabled. True if mirroring is enabled; otherwise, false.

### -param pFlipHorizontal [out]

Type: <b>BOOL*</b>

A pointer to a boolean value indicating whether the stream is being flipped horizontally. True if the stream is being flipped horizontally; otherwise, false.

### -param pFlipVertical [out]

Type: <b>BOOL*</b>

A pointer to a boolean value indicating whether the stream is being flipped vertically. True if the stream is being flipped vertically; otherwise, false.

## -see-also

<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11videocontext1">ID3D11VideoContext1</a>