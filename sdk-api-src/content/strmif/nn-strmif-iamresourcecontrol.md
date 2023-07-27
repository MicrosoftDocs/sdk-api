---
UID: NN:strmif.IAMResourceControl
title: IAMResourceControl (strmif.h)
description: The IAMResourceControl interface opens and holds an audio device resource before the device is actually needed, so that playback can be guaranteed or the application can learn in advance that a device is not available.The following filters implement this interface:Audio Capture filter.DirectSound Renderer filter.Audio Renderer (WaveOut) filter.
helpviewer_keywords: ["IAMResourceControl","IAMResourceControl interface [DirectShow]","IAMResourceControl interface [DirectShow]","described","IAMResourceControlInterface","dshow.iamresourcecontrol","strmif/IAMResourceControl"]
old-location: dshow\iamresourcecontrol.htm
tech.root: dshow
ms.assetid: 9b0b6b46-bf61-44c2-981a-44df4d7c6dfb
ms.date: 4/26/2023
ms.keywords: IAMResourceControl, IAMResourceControl interface [DirectShow], IAMResourceControl interface [DirectShow],described, IAMResourceControlInterface, dshow.iamresourcecontrol, strmif/IAMResourceControl
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IAMResourceControl
 - strmif/IAMResourceControl
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
 - IAMResourceControl
---

# IAMResourceControl interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IAMResourceControl</code> interface opens and holds an audio device resource before the device is actually needed, so that playback can be guaranteed or the application can learn in advance that a device is not available.

The following filters implement this interface:

<ul>
<li>
<a href="/windows/desktop/DirectShow/audio-capture-filter">Audio Capture</a> filter.</li>
<li>
<a href="/windows/desktop/DirectShow/directsound-renderer-filter">DirectSound Renderer</a> filter.</li>
<li>
<a href="/windows/desktop/DirectShow/audio-renderer--waveout--filter">Audio Renderer (WaveOut)</a> filter.</li>
</ul>

## -inheritance

The <b>IAMResourceControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMResourceControl</b> also has these types of members:

