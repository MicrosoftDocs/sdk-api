---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetStreamSourceRect
title: ID3D11VideoContext::VideoProcessorGetStreamSourceRect (d3d11.h)
description: Gets the source rectangle for an input stream on the video processor.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorGetStreamSourceRect method","ID3D11VideoContext.VideoProcessorGetStreamSourceRect","ID3D11VideoContext::VideoProcessorGetStreamSourceRect","VideoProcessorGetStreamSourceRect","VideoProcessorGetStreamSourceRect method [Media Foundation]","VideoProcessorGetStreamSourceRect method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorGetStreamSourceRect","mf.id3d11videocontext_videoprocessorgetstreamsourcerect"]
old-location: mf\id3d11videocontext_videoprocessorgetstreamsourcerect.htm
tech.root: mf
ms.assetid: 52AFE959-695B-4797-ABCF-B8264046E4BE
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetStreamSourceRect method, ID3D11VideoContext.VideoProcessorGetStreamSourceRect, ID3D11VideoContext::VideoProcessorGetStreamSourceRect, VideoProcessorGetStreamSourceRect, VideoProcessorGetStreamSourceRect method [Media Foundation], VideoProcessorGetStreamSourceRect method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetStreamSourceRect, mf.id3d11videocontext_videoprocessorgetstreamsourcerect
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
 - ID3D11VideoContext::VideoProcessorGetStreamSourceRect
 - d3d11/ID3D11VideoContext::VideoProcessorGetStreamSourceRect
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
 - ID3D11VideoContext.VideoProcessorGetStreamSourceRect
---

# ID3D11VideoContext::VideoProcessorGetStreamSourceRect


## -description

Gets the source rectangle for an input stream on the video processor.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.

### -param pEnabled [out]

Receives the value <b>TRUE</b> if the source rectangle is enabled, or <b>FALSE</b> otherwise.

### -param pRect [out]

A pointer to a <a href="/windows/win32/api/windef/ns-windef-rect">RECT</a> structure that receives the source rectangle.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>