---
UID: NN:amaudio.IAMDirectSound
title: IAMDirectSound (amaudio.h)
description: The IAMDirectSound interface specifies which window has focus for controlling DirectSound audio playback.
helpviewer_keywords: ["IAMDirectSound","IAMDirectSound interface [DirectShow]","IAMDirectSound interface [DirectShow]","described","IAMDirectSoundInterface","amaudio/IAMDirectSound","dshow.iamdirectsound"]
old-location: dshow\iamdirectsound.htm
tech.root: dshow
ms.assetid: a9afaeb7-e2d4-4dbf-9f4d-144cafbd5e28
ms.date: 12/05/2018
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

The <code>IAMDirectSound</code> interface specifies which window has focus for controlling DirectSound audio playback. DirectShow provides limited support for this interface:

<ul>
<li>The <a href="/windows/desktop/DirectShow/directsound-renderer-filter">DirectSound Renderer</a> implements the <b>GetFocusWindow</b> and <b>SetFocusWindow</b> methods. It does not implement the other methods on the interface.</li>
<li>The <a href="/windows/desktop/DirectShow/audio-renderer--waveout--filter">Audio Renderer (WaveOut)</a> exposes the interface but does not implement any of its methods.</li>
</ul>

## -inheritance

The <b>IAMDirectSound</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMDirectSound</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
