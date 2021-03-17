---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetOutputStereoMode
title: ID3D11VideoContext::VideoProcessorGetOutputStereoMode (d3d11.h)
description: Queries whether the video processor produces stereo video frames.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorGetOutputStereoMode method","ID3D11VideoContext.VideoProcessorGetOutputStereoMode","ID3D11VideoContext::VideoProcessorGetOutputStereoMode","VideoProcessorGetOutputStereoMode","VideoProcessorGetOutputStereoMode method [Media Foundation]","VideoProcessorGetOutputStereoMode method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorGetOutputStereoMode","mf.id3d11videocontext_videoprocessorgetoutputstereomode"]
old-location: mf\id3d11videocontext_videoprocessorgetoutputstereomode.htm
tech.root: mf
ms.assetid: E7BDB9DA-2760-416D-BD51-F73A035B790A
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetOutputStereoMode method, ID3D11VideoContext.VideoProcessorGetOutputStereoMode, ID3D11VideoContext::VideoProcessorGetOutputStereoMode, VideoProcessorGetOutputStereoMode, VideoProcessorGetOutputStereoMode method [Media Foundation], VideoProcessorGetOutputStereoMode method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetOutputStereoMode, mf.id3d11videocontext_videoprocessorgetoutputstereomode
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
 - ID3D11VideoContext::VideoProcessorGetOutputStereoMode
 - d3d11/ID3D11VideoContext::VideoProcessorGetOutputStereoMode
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
 - ID3D11VideoContext.VideoProcessorGetOutputStereoMode
---

# ID3D11VideoContext::VideoProcessorGetOutputStereoMode


## -description

Queries whether the video processor produces stereo video frames.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param pEnabled [out]

Receives the value <b>TRUE</b> if stereo output is enabled, or <b>FALSE</b> otherwise.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>