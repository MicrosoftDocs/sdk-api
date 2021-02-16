---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetOutputColorSpace
title: ID3D11VideoContext::VideoProcessorGetOutputColorSpace (d3d11.h)
description: Gets the current output color space for the video processor.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorGetOutputColorSpace method","ID3D11VideoContext.VideoProcessorGetOutputColorSpace","ID3D11VideoContext::VideoProcessorGetOutputColorSpace","VideoProcessorGetOutputColorSpace","VideoProcessorGetOutputColorSpace method [Media Foundation]","VideoProcessorGetOutputColorSpace method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorGetOutputColorSpace","mf.id3d11videocontext_videoprocessorgetoutputcolorspace"]
old-location: mf\id3d11videocontext_videoprocessorgetoutputcolorspace.htm
tech.root: mf
ms.assetid: 26D9C908-D8A6-44F9-895F-48C52F4C8B59
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetOutputColorSpace method, ID3D11VideoContext.VideoProcessorGetOutputColorSpace, ID3D11VideoContext::VideoProcessorGetOutputColorSpace, VideoProcessorGetOutputColorSpace, VideoProcessorGetOutputColorSpace method [Media Foundation], VideoProcessorGetOutputColorSpace method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetOutputColorSpace, mf.id3d11videocontext_videoprocessorgetoutputcolorspace
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
 - ID3D11VideoContext::VideoProcessorGetOutputColorSpace
 - d3d11/ID3D11VideoContext::VideoProcessorGetOutputColorSpace
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
 - ID3D11VideoContext.VideoProcessorGetOutputColorSpace
---

# ID3D11VideoContext::VideoProcessorGetOutputColorSpace


## -description

Gets the current output color space for the video processor.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param pColorSpace [out]

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_color_space">D3D11_VIDEO_PROCESSOR_COLOR_SPACE</a> structure. The method fills in the structure with the output color space.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>