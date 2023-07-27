---
UID: NN:strmif.IAMClockSlave
title: IAMClockSlave (strmif.h)
description: The IAMClockSlave interface controls the tolerance of an audio renderer when it is matching rates with another clock.If the audio renderer is matching rates with another clock, it allows the audio to drift up to the amount of the specified tolerance.
helpviewer_keywords: ["IAMClockSlave","IAMClockSlave interface [DirectShow]","IAMClockSlave interface [DirectShow]","described","IAMClockSlaveInterface","dshow.iamclockslave","strmif/IAMClockSlave"]
old-location: dshow\iamclockslave.htm
tech.root: dshow
ms.assetid: 7b3d0f93-09dd-4a36-a031-70f61402c314
ms.date: 4/26/2023
ms.keywords: IAMClockSlave, IAMClockSlave interface [DirectShow], IAMClockSlave interface [DirectShow],described, IAMClockSlaveInterface, dshow.iamclockslave, strmif/IAMClockSlave
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
 - IAMClockSlave
 - strmif/IAMClockSlave
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
 - IAMClockSlave
---

# IAMClockSlave interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IAMClockSlave</code> interface controls the tolerance of an audio renderer when it is matching rates with another clock.

If the audio renderer is matching rates with another clock, it allows the audio to drift up to the amount of the specified tolerance. If the audio drifts too far ahead, the renderer drops samples; if it drifts too far behind, the renderer inserts silent gaps. This interface enables an application to change the tolerance from the default.

Setting a larger tolerance is likely to result in the audio stream becoming out of sync with the video stream. Setting a smaller tolerance can cause audio jitter. Therefore, changing the tolerance setting is not recommended, unless you have a specific reason to do so.

## -inheritance

The <b>IAMClockSlave</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMClockSlave</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/live-sources">Live Sources</a>
