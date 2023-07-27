---
UID: NN:strmif.IDDrawExclModeVideo
title: IDDrawExclModeVideo (strmif.h)
description: The IDDrawExclModeVideo interface enables video playback in DirectDraw exclusive full-screen mode.
helpviewer_keywords: ["IDDrawExclModeVideo","IDDrawExclModeVideo interface [DirectShow]","IDDrawExclModeVideo interface [DirectShow]","described","IDDrawExclModeVideoInterface","dshow.iddrawexclmodevideo","strmif/IDDrawExclModeVideo"]
old-location: dshow\iddrawexclmodevideo.htm
tech.root: dshow
ms.assetid: 6a846a07-f513-49e7-85e8-192a5c211515
ms.date: 4/26/2023
ms.keywords: IDDrawExclModeVideo, IDDrawExclModeVideo interface [DirectShow], IDDrawExclModeVideo interface [DirectShow],described, IDDrawExclModeVideoInterface, dshow.iddrawexclmodevideo, strmif/IDDrawExclModeVideo
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
 - IDDrawExclModeVideo
 - strmif/IDDrawExclModeVideo
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
 - IDDrawExclModeVideo
---

# IDDrawExclModeVideo interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IDDrawExclModeVideo</code> interface enables video playback in DirectDraw exclusive full-screen mode. The <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer Filter</a> implements this interface. Game applications can use DirectDraw in exclusive full-screen mode and continue playing video. For example, the video can be in the background and graphics can be used on top of it. The application passes in a DirectDraw object and primary surface, and these are passed to the Overlay Mixer filter in the filter graph.

The DVD graph builder object uses <code>IDDrawExclModeVideo</code> to play DVD content while in DirectDraw exclusive full-screen mode. This interface can also be used alone to play MPEG-1 or AVI videos in games.

## -inheritance

The <b>IDDrawExclModeVideo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDDrawExclModeVideo</b> also has these types of members:

