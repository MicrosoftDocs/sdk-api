---
UID: NN:strmif.IAMAudioRendererStats
title: IAMAudioRendererStats (strmif.h)
description: The IAMAudioRendererStats interface retrieves statistical performance information from an audio renderer filter.This interface is intended for use during development, to log performance data from the audio renderer.
helpviewer_keywords: ["IAMAudioRendererStats","IAMAudioRendererStats interface [DirectShow]","IAMAudioRendererStats interface [DirectShow]","described","IAMAudioRendererStatsInterface","dshow.iamaudiorendererstats","strmif/IAMAudioRendererStats"]
old-location: dshow\iamaudiorendererstats.htm
tech.root: dshow
ms.assetid: f5cca658-73ce-4f4d-8992-afb7824f4117
ms.date: 4/26/2023
ms.keywords: IAMAudioRendererStats, IAMAudioRendererStats interface [DirectShow], IAMAudioRendererStats interface [DirectShow],described, IAMAudioRendererStatsInterface, dshow.iamaudiorendererstats, strmif/IAMAudioRendererStats
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
 - IAMAudioRendererStats
 - strmif/IAMAudioRendererStats
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
 - IAMAudioRendererStats
---

# IAMAudioRendererStats interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IAMAudioRendererStats</code> interface retrieves statistical performance information from an audio renderer filter.

This interface is intended for use during development, to log performance data from the audio renderer. There is probably no reason for an application to use it in a retail build. The <a href="/windows/desktop/DirectShow/audio-renderer--waveout--filter">Audio Renderer (WaveOut)</a> filter and the <a href="/windows/desktop/DirectShow/directsound-renderer-filter">DirectSound Renderer</a> filter both expose this interface.

<b>Filter Developers</b>: It is not expected that other filters will implement this interface.

## -inheritance

The <b>IAMAudioRendererStats</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMAudioRendererStats</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
