---
UID: NN:strmif.IVideoFrameStep
title: IVideoFrameStep (strmif.h)
description: The IVideoFrameStep interface steps through a video stream.
helpviewer_keywords: ["IVideoFrameStep","IVideoFrameStep interface [DirectShow]","IVideoFrameStep interface [DirectShow]","described","IVideoFrameStepInterface","dshow.ivideoframestep","strmif/IVideoFrameStep"]
old-location: dshow\ivideoframestep.htm
tech.root: dshow
ms.assetid: 7bf45473-144c-49f8-8178-aff5b60112b6
ms.date: 12/05/2018
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

The <code>IVideoFrameStep</code> interface steps through a video stream. This interface enables Microsoft® DirectShow® applications, including DVD players, to step through a video stream as slowly as one frame at a time. Obtain the interface through the filter graph manager, which controls the frame stepping process in conjunction with the <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer Filter</a> or the Video Renderer Filter. Backward frame stepping is not supported.

<div class="alert"><b>Note</b>  For frame stepping to work with a hardware decoder, the decoder must support the <a href="/windows/desktop/DirectShow/frame-stepping-property-set">Frame Stepping Property Set</a>.</div>
<div> </div>

## -inheritance

The <b>IVideoFrameStep</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVideoFrameStep</b> also has these types of members:

