---
UID: NN:strmif.IAMOverlayFX
title: IAMOverlayFX (strmif.h)
description: The IAMOverlayFX interface controls how the video overlay appears on the user's screen. The Overlay Mixer filter implements this interface.
helpviewer_keywords: ["IAMOverlayFX","IAMOverlayFX interface [DirectShow]","IAMOverlayFX interface [DirectShow]","described","IAMOverlayFXInterface","dshow.iamoverlayfx","strmif/IAMOverlayFX"]
old-location: dshow\iamoverlayfx.htm
tech.root: dshow
ms.assetid: 6bc78464-8c9e-4016-b9aa-6589d53d45bf
ms.date: 4/26/2023
ms.keywords: IAMOverlayFX, IAMOverlayFX interface [DirectShow], IAMOverlayFX interface [DirectShow],described, IAMOverlayFXInterface, dshow.iamoverlayfx, strmif/IAMOverlayFX
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
 - IAMOverlayFX
 - strmif/IAMOverlayFX
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
 - IAMOverlayFX
---

# IAMOverlayFX interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IAMOverlayFX</code> interface controls how the video overlay appears on the user's screen. The <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter implements this interface.

## -inheritance

The <b>IAMOverlayFX</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMOverlayFX</b> also has these types of members:

