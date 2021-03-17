---
UID: NF:d3d11_1.ID3D11VideoContext1.VideoProcessorSetStreamMirror
title: ID3D11VideoContext1::VideoProcessorSetStreamMirror (d3d11_1.h)
description: Specifies whether the video processor input stream should be flipped vertically or horizontally.
helpviewer_keywords: ["ID3D11VideoContext1 interface [Media Foundation]","VideoProcessorSetStreamMirror method","ID3D11VideoContext1.VideoProcessorSetStreamMirror","ID3D11VideoContext1::VideoProcessorSetStreamMirror","VideoProcessorSetStreamMirror","VideoProcessorSetStreamMirror method [Media Foundation]","VideoProcessorSetStreamMirror method [Media Foundation]","ID3D11VideoContext1 interface","d3d11_1/ID3D11VideoContext1::VideoProcessorSetStreamMirror","mf.id3d11videocontext1_videoprocessorsetstreammirror"]
old-location: mf\id3d11videocontext1_videoprocessorsetstreammirror.htm
tech.root: mf
ms.assetid: C8CCCC2B-B05A-4AF4-9274-1E205B9807DB
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext1 interface [Media Foundation],VideoProcessorSetStreamMirror method, ID3D11VideoContext1.VideoProcessorSetStreamMirror, ID3D11VideoContext1::VideoProcessorSetStreamMirror, VideoProcessorSetStreamMirror, VideoProcessorSetStreamMirror method [Media Foundation], VideoProcessorSetStreamMirror method [Media Foundation],ID3D11VideoContext1 interface, d3d11_1/ID3D11VideoContext1::VideoProcessorSetStreamMirror, mf.id3d11videocontext1_videoprocessorsetstreammirror
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
 - ID3D11VideoContext1::VideoProcessorSetStreamMirror
 - d3d11_1/ID3D11VideoContext1::VideoProcessorSetStreamMirror
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
 - ID3D11VideoContext1.VideoProcessorSetStreamMirror
---

# ID3D11VideoContext1::VideoProcessorSetStreamMirror


## -description

Specifies whether the video processor input stream should be flipped vertically or horizontally.

## -parameters

### -param pVideoProcessor [in]

Type: <b>ID3D11VideoProcessor*</b>

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface.

### -param StreamIndex [in]

Type: <b>UINT</b>

An index identifying the input stream.

### -param Enable [in]

Type: <b>BOOL</b>

True if mirroring should be enabled; otherwise, false.

### -param FlipHorizontal [in]

Type: <b>BOOL</b>

True if the stream should be flipped horizontally; otherwise, false.

### -param FlipVertical [in]

Type: <b>BOOL</b>

True if the stream should be flipped vertically; otherwise, false.

## -remarks

When used in combination, transformations on the processor input stream should be applied in the following order:

<ul>
<li>Rotation</li>
<li>Mirroring</li>
<li>Source clipping</li>
</ul>

## -see-also

<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11videocontext1">ID3D11VideoContext1</a>