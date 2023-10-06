---
UID: NN:strmif.IVideoFrameStep
title: IVideoFrameStep (strmif.h)
description: The IVideoFrameStep interface steps through a video stream.
helpviewer_keywords: ["IVideoFrameStep","IVideoFrameStep interface [DirectShow]","IVideoFrameStep interface [DirectShow]","described","IVideoFrameStepInterface","dshow.ivideoframestep","strmif/IVideoFrameStep"]
old-location: dshow\ivideoframestep.htm
tech.root: dshow
ms.assetid: 7bf45473-144c-49f8-8178-aff5b60112b6
ms.date: 4/26/2023
ms.keywords: IVideoFrameStep, IVideoFrameStep interface [DirectShow], IVideoFrameStep interface [DirectShow],described, IVideoFrameStepInterface, dshow.ivideoframestep, strmif/IVideoFrameStep
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVideoFrameStep
 - strmif/IVideoFrameStep
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVideoFrameStep
---

# IVideoFrameStep interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IVideoFrameStep</code> interface steps through a video stream. This interface enables Microsoft® DirectShow® applications, including DVD players, to step through a video stream as slowly as one frame at a time. Obtain the interface through the filter graph manager, which controls the frame stepping process in conjunction with the <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer Filter</a> or the Video Renderer Filter. Backward frame stepping is not supported.

<div class="alert"><b>Note</b>  For frame stepping to work with a hardware decoder, the decoder must support the <a href="/windows/desktop/DirectShow/frame-stepping-property-set">Frame Stepping Property Set</a>.</div>
<div> </div>

## -inheritance

The <b>IVideoFrameStep</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVideoFrameStep</b> also has these types of members:

