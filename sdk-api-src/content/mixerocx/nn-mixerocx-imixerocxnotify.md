---
UID: NN:mixerocx.IMixerOCXNotify
title: IMixerOCXNotify (mixerocx.h)
description: The IMixerOCXNotify interface is implemented by clients and called by the Overlay Mixer to send notifications of events affecting the video display rectangle.
helpviewer_keywords: ["IMixerOCXNotify","IMixerOCXNotify interface [DirectShow]","IMixerOCXNotify interface [DirectShow]","described","IMixerOCXNotifyInterface","dshow.imixerocxnotify","mixerocx/IMixerOCXNotify"]
old-location: dshow\imixerocxnotify.htm
tech.root: dshow
ms.assetid: b73416c0-2312-4164-8a6d-f8776dc1447f
ms.date: 4/26/2023
ms.keywords: IMixerOCXNotify, IMixerOCXNotify interface [DirectShow], IMixerOCXNotify interface [DirectShow],described, IMixerOCXNotifyInterface, dshow.imixerocxnotify, mixerocx/IMixerOCXNotify
req.header: mixerocx.h
req.include-header: 
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
 - IMixerOCXNotify
 - mixerocx/IMixerOCXNotify
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
 - IMixerOCXNotify
---

# IMixerOCXNotify interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IMixerOCXNotify</code> interface is implemented by clients and called by the Overlay Mixer to send notifications of events affecting the video display rectangle.

## -inheritance

The <b>IMixerOCXNotify</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMixerOCXNotify</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/mixerocx/nn-mixerocx-imixerocx">IMixerOCX Interface</a>
