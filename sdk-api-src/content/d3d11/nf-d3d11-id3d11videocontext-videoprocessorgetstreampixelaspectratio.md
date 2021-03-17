---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetStreamPixelAspectRatio
title: ID3D11VideoContext::VideoProcessorGetStreamPixelAspectRatio (d3d11.h)
description: Gets the pixel aspect ratio for an input stream on the video processor.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorGetStreamPixelAspectRatio method","ID3D11VideoContext.VideoProcessorGetStreamPixelAspectRatio","ID3D11VideoContext::VideoProcessorGetStreamPixelAspectRatio","VideoProcessorGetStreamPixelAspectRatio","VideoProcessorGetStreamPixelAspectRatio method [Media Foundation]","VideoProcessorGetStreamPixelAspectRatio method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorGetStreamPixelAspectRatio","mf.id3d11videocontext_videoprocessorgetstreampixelaspectratio"]
old-location: mf\id3d11videocontext_videoprocessorgetstreampixelaspectratio.htm
tech.root: mf
ms.assetid: 45B0CF31-6552-4C75-B32F-755398D1A054
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetStreamPixelAspectRatio method, ID3D11VideoContext.VideoProcessorGetStreamPixelAspectRatio, ID3D11VideoContext::VideoProcessorGetStreamPixelAspectRatio, VideoProcessorGetStreamPixelAspectRatio, VideoProcessorGetStreamPixelAspectRatio method [Media Foundation], VideoProcessorGetStreamPixelAspectRatio method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetStreamPixelAspectRatio, mf.id3d11videocontext_videoprocessorgetstreampixelaspectratio
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
 - ID3D11VideoContext::VideoProcessorGetStreamPixelAspectRatio
 - d3d11/ID3D11VideoContext::VideoProcessorGetStreamPixelAspectRatio
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
 - ID3D11VideoContext.VideoProcessorGetStreamPixelAspectRatio
---

# ID3D11VideoContext::VideoProcessorGetStreamPixelAspectRatio


## -description

Gets the pixel aspect ratio for an input stream on the video processor.

## -parameters

### -param pVideoProcessor [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.

### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.

### -param pEnabled [out]

Receives the value <b>TRUE</b> if the pixel aspect ratio is specified. Otherwise, receives the value <b>FALSE</b>.

### -param pSourceAspectRatio [out]

A pointer to a <a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_rational">DXGI_RATIONAL</a> structure. If *<i>pEnabled</i> is <b>TRUE</b>, this parameter receives the pixel aspect ratio of the source rectangle.

### -param pDestinationAspectRatio [out]

A pointer to a <a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_rational">DXGI_RATIONAL</a> structure. If *<i>pEnabled</i> is <b>TRUE</b>, this parameter receives the pixel aspect ratio of the destination rectangle.

## -remarks

When the method returns, if <i>*pEnabled</i> is <b>TRUE</b>, the <i>pSourceAspectRatio</i> and <i>pDestinationAspectRatio</i> parameters contain the pixel aspect ratios. Otherwise, the default pixel aspect ratio is 1:1 (square pixels).

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>