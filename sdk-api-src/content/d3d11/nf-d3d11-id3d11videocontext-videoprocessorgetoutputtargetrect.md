---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetOutputTargetRect
title: ID3D11VideoContext::VideoProcessorGetOutputTargetRect (d3d11.h)
description: Gets the current target rectangle for the video processor.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorGetOutputTargetRect method","ID3D11VideoContext.VideoProcessorGetOutputTargetRect","ID3D11VideoContext::VideoProcessorGetOutputTargetRect","VideoProcessorGetOutputTargetRect","VideoProcessorGetOutputTargetRect method [Media Foundation]","VideoProcessorGetOutputTargetRect method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorGetOutputTargetRect","mf.id3d11videocontext_videoprocessorgetoutputtargetrect"]
old-location: mf\id3d11videocontext_videoprocessorgetoutputtargetrect.htm
tech.root: mf
ms.assetid: 5D59822A-B322-4E79-A543-A89C2232C62F
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetOutputTargetRect method, ID3D11VideoContext.VideoProcessorGetOutputTargetRect, ID3D11VideoContext::VideoProcessorGetOutputTargetRect, VideoProcessorGetOutputTargetRect, VideoProcessorGetOutputTargetRect method [Media Foundation], VideoProcessorGetOutputTargetRect method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetOutputTargetRect, mf.id3d11videocontext_videoprocessorgetoutputtargetrect
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
 - ID3D11VideoContext::VideoProcessorGetOutputTargetRect
 - d3d11/ID3D11VideoContext::VideoProcessorGetOutputTargetRect
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
 - ID3D11VideoContext.VideoProcessorGetOutputTargetRect
---

# ID3D11VideoContext::VideoProcessorGetOutputTargetRect


## -description

Gets the current target rectangle for the video processor.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param Enabled [out]

Receives the value <b>TRUE</b> if the target rectangle was explicitly set using the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputtargetrect">ID3D11VideoContext::VideoProcessorSetOutputTargetRect</a> method. Receives the value FALSE if the target rectangle was disabled or was never set.

### -param pRect [out]

If <i>Enabled</i> receives the value <b>TRUE</b>, this parameter receives the target rectangle. Otherwise, this parameter is ignored.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>