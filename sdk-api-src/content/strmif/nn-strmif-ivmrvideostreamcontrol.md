---
UID: NN:strmif.IVMRVideoStreamControl
title: IVMRVideoStreamControl (strmif.h)
description: The IVMRVideoStreamControl interface is implemented on each input pin of the Video Mixing Renderer Filter 7 (VMR-7).
helpviewer_keywords: ["IVMRVideoStreamControl","IVMRVideoStreamControl interface [DirectShow]","IVMRVideoStreamControl interface [DirectShow]","described","IVMRVideoStreamControlInterface","dshow.ivmrvideostreamcontrol","strmif/IVMRVideoStreamControl"]
old-location: dshow\ivmrvideostreamcontrol.htm
tech.root: dshow
ms.assetid: b42fa81e-99d7-4051-b909-2189581825d0
ms.date: 4/26/2023
ms.keywords: IVMRVideoStreamControl, IVMRVideoStreamControl interface [DirectShow], IVMRVideoStreamControl interface [DirectShow],described, IVMRVideoStreamControlInterface, dshow.ivmrvideostreamcontrol, strmif/IVMRVideoStreamControl
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IVMRVideoStreamControl
 - strmif/IVMRVideoStreamControl
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
 - IVMRVideoStreamControl
---

# IVMRVideoStreamControl interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IVMRVideoStreamControl</code> interface is implemented on each input pin of the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7). The interface operates on the input stream represented by the pin. This interface is used by upstream filters (typically decoders) to get or set the active state of individual streams, or the source color key for the composited image. Applications in general should not use this interface.

The VMR-9 input pins expose the <a href="/previous-versions/ms787140(v=vs.85)">IVMRVideoStreamControl9</a> interface.

## -inheritance

The <b>IVMRVideoStreamControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRVideoStreamControl</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
