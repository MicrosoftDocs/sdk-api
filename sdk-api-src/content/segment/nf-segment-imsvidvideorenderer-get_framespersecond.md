---
UID: NF:segment.IMSVidVideoRenderer.get_FramesPerSecond
title: IMSVidVideoRenderer::get_FramesPerSecond (segment.h)
description: The get_FramesPerSecond method retrieves the current frame rate.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","get_FramesPerSecond method","IMSVidVideoRenderer.get_FramesPerSecond","IMSVidVideoRenderer::get_FramesPerSecond","IMSVidVideoRendererget_FramesPerSecond","get_FramesPerSecond","get_FramesPerSecond method [Microsoft TV Technologies]","get_FramesPerSecond method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","mstv.imsvidvideorenderer_get_framespersecond","segment/IMSVidVideoRenderer::get_FramesPerSecond"]
old-location: mstv\imsvidvideorenderer_get_framespersecond.htm
tech.root: mstv
ms.assetid: 94634499-748d-42d1-8d06-fb52d10d4656
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get_FramesPerSecond method, IMSVidVideoRenderer.get_FramesPerSecond, IMSVidVideoRenderer::get_FramesPerSecond, IMSVidVideoRendererget_FramesPerSecond, get_FramesPerSecond, get_FramesPerSecond method [Microsoft TV Technologies], get_FramesPerSecond method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get_framespersecond, segment/IMSVidVideoRenderer::get_FramesPerSecond
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - IMSVidVideoRenderer::get_FramesPerSecond
 - segment/IMSVidVideoRenderer::get_FramesPerSecond
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidVideoRenderer.get_FramesPerSecond
---

# IMSVidVideoRenderer::get_FramesPerSecond


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_FramesPerSecond</b> method retrieves the current frame rate.

## -parameters

### -param pVal [out]

Receives the frame rate, in frames per second.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>