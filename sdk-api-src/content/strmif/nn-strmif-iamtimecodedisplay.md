---
UID: NN:strmif.IAMTimecodeDisplay
title: IAMTimecodeDisplay (strmif.h)
description: The IAMTimecodeDisplay interface controls an external SMPTE/MIDI timecode display device.DirectShow currently does not provide any filters that implement this interface.
helpviewer_keywords: ["IAMTimecodeDisplay","IAMTimecodeDisplay interface [DirectShow]","IAMTimecodeDisplay interface [DirectShow]","described","IAMTimecodeDisplayInterface","dshow.iamtimecodedisplay","strmif/IAMTimecodeDisplay"]
old-location: dshow\iamtimecodedisplay.htm
tech.root: dshow
ms.assetid: 2edfc260-5bb6-475d-b8af-252e7c7a8552
ms.date: 4/26/2023
ms.keywords: IAMTimecodeDisplay, IAMTimecodeDisplay interface [DirectShow], IAMTimecodeDisplay interface [DirectShow],described, IAMTimecodeDisplayInterface, dshow.iamtimecodedisplay, strmif/IAMTimecodeDisplay
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
 - IAMTimecodeDisplay
 - strmif/IAMTimecodeDisplay
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
 - IAMTimecodeDisplay
---

# IAMTimecodeDisplay interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IAMTimecodeDisplay</code> interface controls an external SMPTE/MIDI timecode display device.

DirectShow currently does not provide any filters that implement this interface. Third parties should implement this interface on any filter that controls the timecode display of an external timecode reader or generator. Timecode readers or generators can be built into a VCR or can be separate external devices.

This interface is not intended for rendering in a DirectShow filter graph; it is purely for use on external device displays.

<b>Hardware Requirements</b>

See the <a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport</a> interface for hardware requirements.

## -inheritance

The <b>IAMTimecodeDisplay</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMTimecodeDisplay</b> also has these types of members:

