---
UID: NN:amaudio.IAMDirectSound
title: IAMDirectSound (amaudio.h)
description: The IAMDirectSound interface specifies which window has focus for controlling DirectSound audio playback.
helpviewer_keywords: ["IAMDirectSound","IAMDirectSound interface [DirectShow]","IAMDirectSound interface [DirectShow]","described","IAMDirectSoundInterface","amaudio/IAMDirectSound","dshow.iamdirectsound"]
old-location: dshow\iamdirectsound.htm
tech.root: dshow
ms.assetid: a9afaeb7-e2d4-4dbf-9f4d-144cafbd5e28
ms.date: 4/26/2023
ms.keywords: IAMDirectSound, IAMDirectSound interface [DirectShow], IAMDirectSound interface [DirectShow],described, IAMDirectSoundInterface, amaudio/IAMDirectSound, dshow.iamdirectsound
req.header: amaudio.h
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
 - IAMDirectSound
 - amaudio/IAMDirectSound
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
 - IAMDirectSound
---

# IAMDirectSound interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IAMDirectSound</code> interface specifies which window has focus for controlling DirectSound audio playback. DirectShow provides limited support for this interface:

<ul>
<li>The <a href="/windows/desktop/DirectShow/directsound-renderer-filter">DirectSound Renderer</a> implements the <b>GetFocusWindow</b> and <b>SetFocusWindow</b> methods. It does not implement the other methods on the interface.</li>
<li>The <a href="/windows/desktop/DirectShow/audio-renderer--waveout--filter">Audio Renderer (WaveOut)</a> exposes the interface but does not implement any of its methods.</li>
</ul>

## -inheritance

The <b>IAMDirectSound</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMDirectSound</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
