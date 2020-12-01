---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetOutputConstriction
title: ID3D11VideoContext::VideoProcessorGetOutputConstriction (d3d11.h)
description: Gets the current level of downsampling that is performed by the video processor.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorGetOutputConstriction method","ID3D11VideoContext.VideoProcessorGetOutputConstriction","ID3D11VideoContext::VideoProcessorGetOutputConstriction","VideoProcessorGetOutputConstriction","VideoProcessorGetOutputConstriction method [Media Foundation]","VideoProcessorGetOutputConstriction method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorGetOutputConstriction","mf.id3d11videocontext_videoprocessorgetoutputconstriction"]
old-location: mf\id3d11videocontext_videoprocessorgetoutputconstriction.htm
tech.root: mf
ms.assetid: 40F7D380-C385-4C1C-90E5-E362CA54CD41
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetOutputConstriction method, ID3D11VideoContext.VideoProcessorGetOutputConstriction, ID3D11VideoContext::VideoProcessorGetOutputConstriction, VideoProcessorGetOutputConstriction, VideoProcessorGetOutputConstriction method [Media Foundation], VideoProcessorGetOutputConstriction method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetOutputConstriction, mf.id3d11videocontext_videoprocessorgetoutputconstriction
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
 - ID3D11VideoContext::VideoProcessorGetOutputConstriction
 - d3d11/ID3D11VideoContext::VideoProcessorGetOutputConstriction
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
 - ID3D11VideoContext.VideoProcessorGetOutputConstriction
---

# ID3D11VideoContext::VideoProcessorGetOutputConstriction


## -description

Gets the current level of downsampling that is performed by the video processor.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param pEnabled [out]

Receives the value <b>TRUE</b> if downsampling was explicitly enabled using the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputconstriction">ID3D11VideoContext::VideoProcessorSetOutputConstriction</a> method. Receives the value <b>FALSE</b> if the downsampling was disabled or was never set.

### -param pSize [out]

If <i>Enabled</i> receives the value <b>TRUE</b>, this parameter receives the downsampling size. Otherwise, this parameter is ignored.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>