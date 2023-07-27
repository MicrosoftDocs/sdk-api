---
UID: NN:mixerocx.IMixerOCX
title: IMixerOCX (mixerocx.h)
description: The IMixerOCX interface is implemented on the Overlay Mixer.
helpviewer_keywords: ["IMixerOCX","IMixerOCX interface [DirectShow]","IMixerOCX interface [DirectShow]","described","IMixerOCXInterface","dshow.imixerocx","mixerocx/IMixerOCX"]
old-location: dshow\imixerocx.htm
tech.root: dshow
ms.assetid: b80d720d-921d-4d24-a168-49944cfcc411
ms.date: 4/26/2023
ms.keywords: IMixerOCX, IMixerOCX interface [DirectShow], IMixerOCX interface [DirectShow],described, IMixerOCXInterface, dshow.imixerocx, mixerocx/IMixerOCX
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
 - IMixerOCX
 - mixerocx/IMixerOCX
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
 - IMixerOCX
---

# IMixerOCX interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IMixerOCX</code> interface is implemented on the <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a>. This interface enables clients that do not own their own windows, such as an ActiveX control, to set properties of the video rectangle and advise the filter of events.

<div class="alert"><b>Note</b>  Applications should generally use the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a> (VMR-9) and not the Overlay Mixer. The only scenario that requires the Overlay Mixer is when the video capture or decoder hardware uses video ports to transfer video data to the graphics card. The VMR-9 does not support video ports.</div>
<div> </div>

## -inheritance

The <b>IMixerOCX</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMixerOCX</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

