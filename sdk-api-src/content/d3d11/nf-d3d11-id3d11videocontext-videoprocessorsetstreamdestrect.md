---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamDestRect
title: ID3D11VideoContext::VideoProcessorSetStreamDestRect (d3d11.h)
description: Sets the destination rectangle for an input stream on the video processor.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorSetStreamDestRect method","ID3D11VideoContext.VideoProcessorSetStreamDestRect","ID3D11VideoContext::VideoProcessorSetStreamDestRect","VideoProcessorSetStreamDestRect","VideoProcessorSetStreamDestRect method [Media Foundation]","VideoProcessorSetStreamDestRect method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorSetStreamDestRect","mf.id3d11videocontext_videoprocessorsetstreamdestrect"]
old-location: mf\id3d11videocontext_videoprocessorsetstreamdestrect.htm
tech.root: mf
ms.assetid: F3C77812-9096-4D65-9D6C-082133C873A7
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamDestRect method, ID3D11VideoContext.VideoProcessorSetStreamDestRect, ID3D11VideoContext::VideoProcessorSetStreamDestRect, VideoProcessorSetStreamDestRect, VideoProcessorSetStreamDestRect method [Media Foundation], VideoProcessorSetStreamDestRect method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamDestRect, mf.id3d11videocontext_videoprocessorsetstreamdestrect
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
 - ID3D11VideoContext::VideoProcessorSetStreamDestRect
 - d3d11/ID3D11VideoContext::VideoProcessorSetStreamDestRect
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
 - ID3D11VideoContext.VideoProcessorSetStreamDestRect
---

# ID3D11VideoContext::VideoProcessorSetStreamDestRect


## -description

Sets the destination rectangle for an input stream on the video processor.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.

### -param Enable [in]

Specifies whether to apply the destination rectangle.

### -param pRect [in]

A pointer to a <a href="/windows/win32/api/windef/ns-windef-rect">RECT</a> structure that specifies the destination rectangle. If <i>Enable</i> is <b>FALSE</b>, this parameter is ignored.

## -remarks

The destination rectangle is the portion of the output surface that receives the blit for this stream. The destination rectangle is given in pixel coordinates, relative to the output surface.

The default destination rectangle is an empty rectangle (0, 0, 0, 0). If this method is never called, or if the <i>Enable</i> parameter is <b>FALSE</b>, no data is written from this stream.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>