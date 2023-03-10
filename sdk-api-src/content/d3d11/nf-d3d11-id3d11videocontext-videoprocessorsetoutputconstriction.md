---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetOutputConstriction
title: ID3D11VideoContext::VideoProcessorSetOutputConstriction (d3d11.h)
description: Sets the amount of downsampling to perform on the output.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorSetOutputConstriction method","ID3D11VideoContext.VideoProcessorSetOutputConstriction","ID3D11VideoContext::VideoProcessorSetOutputConstriction","VideoProcessorSetOutputConstriction","VideoProcessorSetOutputConstriction method [Media Foundation]","VideoProcessorSetOutputConstriction method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorSetOutputConstriction","mf.id3d11videocontext_videoprocessorsetoutputconstriction"]
old-location: mf\id3d11videocontext_videoprocessorsetoutputconstriction.htm
tech.root: mf
ms.assetid: EA61A4B8-0853-4F17-B634-70A896DCF5F7
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetOutputConstriction method, ID3D11VideoContext.VideoProcessorSetOutputConstriction, ID3D11VideoContext::VideoProcessorSetOutputConstriction, VideoProcessorSetOutputConstriction, VideoProcessorSetOutputConstriction method [Media Foundation], VideoProcessorSetOutputConstriction method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetOutputConstriction, mf.id3d11videocontext_videoprocessorsetoutputconstriction
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
 - ID3D11VideoContext::VideoProcessorSetOutputConstriction
 - d3d11/ID3D11VideoContext::VideoProcessorSetOutputConstriction
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
 - ID3D11VideoContext.VideoProcessorSetOutputConstriction
---

# ID3D11VideoContext::VideoProcessorSetOutputConstriction


## -description

Sets the amount of downsampling to perform on the output.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param Enable

If <b>TRUE</b>, downsampling is enabled. Otherwise, downsampling is disabled and the <b>Size</b> member is ignored.

### -param Size

The sampling size.

## -remarks

Downsampling is sometimes used to reduce the quality of premium content when other forms of content protection are not available. By default, downsampling is disabled.

If the <i>Enable</i> parameter is <b>TRUE</b>, the driver downsamples the composed image  to the specified size, and then scales it back to the size of the target rectangle.

The width and height of <i>Size</i> must be greater than zero. If the size is larger than the target rectangle, downsampling does not occur.

To use this feature, the driver must support downsampling, indicated by the <b>D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_CONSTRICTION</b> capability flag. To query for this capability, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>