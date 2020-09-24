---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetStreamAlpha
title: ID3D11VideoContext::VideoProcessorGetStreamAlpha (d3d11.h)
description: Gets the planar alpha for an input stream on the video processor.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorGetStreamAlpha method","ID3D11VideoContext.VideoProcessorGetStreamAlpha","ID3D11VideoContext::VideoProcessorGetStreamAlpha","VideoProcessorGetStreamAlpha","VideoProcessorGetStreamAlpha method [Media Foundation]","VideoProcessorGetStreamAlpha method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorGetStreamAlpha","mf.id3d11videocontext_videoprocessorgetstreamalpha"]
old-location: mf\id3d11videocontext_videoprocessorgetstreamalpha.htm
tech.root: mf
ms.assetid: E2DB0672-54D9-4DDB-B6EA-9935237C33FB
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetStreamAlpha method, ID3D11VideoContext.VideoProcessorGetStreamAlpha, ID3D11VideoContext::VideoProcessorGetStreamAlpha, VideoProcessorGetStreamAlpha, VideoProcessorGetStreamAlpha method [Media Foundation], VideoProcessorGetStreamAlpha method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetStreamAlpha, mf.id3d11videocontext_videoprocessorgetstreamalpha
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
 - ID3D11VideoContext::VideoProcessorGetStreamAlpha
 - d3d11/ID3D11VideoContext::VideoProcessorGetStreamAlpha
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
 - ID3D11VideoContext.VideoProcessorGetStreamAlpha
---

# ID3D11VideoContext::VideoProcessorGetStreamAlpha


## -description

Gets the planar alpha for an input stream on the video processor.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.

### -param pEnabled [out]

Receives the value <b>TRUE</b> if planar alpha is enabled, or <b>FALSE</b> otherwise.

### -param pAlpha [out]

Receives the planar alpha value. The value can range from 0.0 (transparent) to 1.0 (opaque).

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>