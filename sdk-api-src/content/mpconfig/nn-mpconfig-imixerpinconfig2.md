---
UID: NN:mpconfig.IMixerPinConfig2
title: IMixerPinConfig2 (mpconfig.h)
description: The IMixerPinConfig2 interface is exposed on the input pins of the Overlay Mixer and contains methods that manipulate video color controls, if the VGA chip supports it.This interface derives from the IMixerPinConfig interface.Applications use this interface to get and set video color controls when mixing multiple video streams.
helpviewer_keywords: ["IMixerPinConfig2","IMixerPinConfig2 interface [DirectShow]","IMixerPinConfig2 interface [DirectShow]","described","IMixerPinConfig2Interface","dshow.imixerpinconfig2","mpconfig/IMixerPinConfig2"]
old-location: dshow\imixerpinconfig2.htm
tech.root: dshow
ms.assetid: d166b139-3ef7-4f47-817a-8f5b644a3776
ms.date: 4/26/2023
ms.keywords: IMixerPinConfig2, IMixerPinConfig2 interface [DirectShow], IMixerPinConfig2 interface [DirectShow],described, IMixerPinConfig2Interface, dshow.imixerpinconfig2, mpconfig/IMixerPinConfig2
req.header: mpconfig.h
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
 - IMixerPinConfig2
 - mpconfig/IMixerPinConfig2
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
 - IMixerPinConfig2
---

# IMixerPinConfig2 interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IMixerPinConfig2</code> interface is exposed on the input pins of the <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> and contains methods that manipulate video color controls, if the VGA chip supports it.

This interface derives from the <a href="/windows/desktop/api/mpconfig/nn-mpconfig-imixerpinconfig">IMixerPinConfig</a> interface.

Applications use this interface to get and set video color controls when mixing multiple video streams.

## -inheritance

The <b>IMixerPinConfig2</b> interface inherits from <a href="/windows/desktop/api/mpconfig/nn-mpconfig-imixerpinconfig">IMixerPinConfig</a>. <b>IMixerPinConfig2</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mpconfig/nn-mpconfig-imixerpinconfig">IMixerPinConfig</a>
