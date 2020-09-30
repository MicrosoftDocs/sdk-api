---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetOutputAlphaFillMode
title: ID3D11VideoContext::VideoProcessorSetOutputAlphaFillMode (d3d11.h)
description: Sets the alpha fill mode for data that the video processor writes to the render target.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorSetOutputAlphaFillMode method","ID3D11VideoContext.VideoProcessorSetOutputAlphaFillMode","ID3D11VideoContext::VideoProcessorSetOutputAlphaFillMode","VideoProcessorSetOutputAlphaFillMode","VideoProcessorSetOutputAlphaFillMode method [Media Foundation]","VideoProcessorSetOutputAlphaFillMode method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorSetOutputAlphaFillMode","mf.id3d11videocontext_videoprocessorsetoutputalphafillmode"]
old-location: mf\id3d11videocontext_videoprocessorsetoutputalphafillmode.htm
tech.root: mf
ms.assetid: 898604FA-B857-4D84-AA0D-3BC517F75A36
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetOutputAlphaFillMode method, ID3D11VideoContext.VideoProcessorSetOutputAlphaFillMode, ID3D11VideoContext::VideoProcessorSetOutputAlphaFillMode, VideoProcessorSetOutputAlphaFillMode, VideoProcessorSetOutputAlphaFillMode method [Media Foundation], VideoProcessorSetOutputAlphaFillMode method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetOutputAlphaFillMode, mf.id3d11videocontext_videoprocessorsetoutputalphafillmode
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
 - ID3D11VideoContext::VideoProcessorSetOutputAlphaFillMode
 - d3d11/ID3D11VideoContext::VideoProcessorSetOutputAlphaFillMode
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
 - ID3D11VideoContext.VideoProcessorSetOutputAlphaFillMode
---

# ID3D11VideoContext::VideoProcessorSetOutputAlphaFillMode


## -description

Sets the alpha fill mode for data that the video processor writes to the render target.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param AlphaFillMode [in]

The alpha fill mode, specified as a <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_alpha_fill_mode">D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE</a> value.

### -param StreamIndex [in]

The zero-based index of an input stream. This parameter is used if <i>AlphaFillMode</i> is <b>D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE_SOURCE_STREAM</b>. Otherwise, the parameter is ignored.

## -remarks

To find out which fill modes the device supports, call the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> method. If the driver reports the <b>D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ALPHA_FILL</b> capability, the driver supports all of the fill modes. Otherwise, the <i>AlphaFillMode</i> parameter must be <b>D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE_OPAQUE</b>.



The default fill mode is <b>D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE_OPAQUE</b>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>