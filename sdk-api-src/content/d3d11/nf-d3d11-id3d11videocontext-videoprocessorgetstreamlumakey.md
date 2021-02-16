---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetStreamLumaKey
title: ID3D11VideoContext::VideoProcessorGetStreamLumaKey (d3d11.h)
description: Gets the luma key for an input stream of the video processor.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorGetStreamLumaKey method","ID3D11VideoContext.VideoProcessorGetStreamLumaKey","ID3D11VideoContext::VideoProcessorGetStreamLumaKey","VideoProcessorGetStreamLumaKey","VideoProcessorGetStreamLumaKey method [Media Foundation]","VideoProcessorGetStreamLumaKey method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorGetStreamLumaKey","mf.id3d11videocontext_videoprocessorgetstreamlumakey"]
old-location: mf\id3d11videocontext_videoprocessorgetstreamlumakey.htm
tech.root: mf
ms.assetid: 1DE22456-84E9-478F-A6CA-4C9CACF7E9AF
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetStreamLumaKey method, ID3D11VideoContext.VideoProcessorGetStreamLumaKey, ID3D11VideoContext::VideoProcessorGetStreamLumaKey, VideoProcessorGetStreamLumaKey, VideoProcessorGetStreamLumaKey method [Media Foundation], VideoProcessorGetStreamLumaKey method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetStreamLumaKey, mf.id3d11videocontext_videoprocessorgetstreamlumakey
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - ID3D11VideoContext::VideoProcessorGetStreamLumaKey
 - d3d11/ID3D11VideoContext::VideoProcessorGetStreamLumaKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoContext.VideoProcessorGetStreamLumaKey
---

# ID3D11VideoContext::VideoProcessorGetStreamLumaKey


## -description

Gets the luma key for an input stream of the video processor.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.

### -param pEnabled [out]

Receives the value <b>TRUE</b> if luma keying is enabled, or <b>FALSE</b> otherwise.

### -param pLower [out]

Receives the lower bound for the luma key. The valid range is [0…1].

### -param pUpper [out]

Receives the upper bound for the luma key. The valid range is [0…1].

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>