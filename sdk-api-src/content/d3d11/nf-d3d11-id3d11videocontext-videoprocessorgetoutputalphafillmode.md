---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetOutputAlphaFillMode
title: ID3D11VideoContext::VideoProcessorGetOutputAlphaFillMode (d3d11.h)
description: Gets the current alpha fill mode for the video processor.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorGetOutputAlphaFillMode method","ID3D11VideoContext.VideoProcessorGetOutputAlphaFillMode","ID3D11VideoContext::VideoProcessorGetOutputAlphaFillMode","VideoProcessorGetOutputAlphaFillMode","VideoProcessorGetOutputAlphaFillMode method [Media Foundation]","VideoProcessorGetOutputAlphaFillMode method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorGetOutputAlphaFillMode","mf.id3d11videocontext_videoprocessorgetoutputalphafillmode"]
old-location: mf\id3d11videocontext_videoprocessorgetoutputalphafillmode.htm
tech.root: mf
ms.assetid: 23F37D9C-3D33-4A07-AC54-5273A09BF540
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetOutputAlphaFillMode method, ID3D11VideoContext.VideoProcessorGetOutputAlphaFillMode, ID3D11VideoContext::VideoProcessorGetOutputAlphaFillMode, VideoProcessorGetOutputAlphaFillMode, VideoProcessorGetOutputAlphaFillMode method [Media Foundation], VideoProcessorGetOutputAlphaFillMode method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetOutputAlphaFillMode, mf.id3d11videocontext_videoprocessorgetoutputalphafillmode
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
 - ID3D11VideoContext::VideoProcessorGetOutputAlphaFillMode
 - d3d11/ID3D11VideoContext::VideoProcessorGetOutputAlphaFillMode
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
 - ID3D11VideoContext.VideoProcessorGetOutputAlphaFillMode
---

# ID3D11VideoContext::VideoProcessorGetOutputAlphaFillMode


## -description

Gets the current alpha fill mode for the video processor.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param pAlphaFillMode [out]

Receives the alpha fill mode, as a <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_alpha_fill_mode">D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE</a> value.

### -param pStreamIndex [out]

If the alpha fill mode is <b>D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE_SOURCE_STREAM</b>, this parameter receives the zero-based index of an input stream. The input stream provides the alpha values for the alpha fill.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>