---
UID: NN:strmif.IAMLatency
title: IAMLatency (strmif.h)
description: The IAMLatency interface reports the amount of latency that a filter introduces into the graph.
helpviewer_keywords: ["IAMLatency","IAMLatency interface [DirectShow]","IAMLatency interface [DirectShow]","described","IAMLatencyInterface","dshow.iamlatency","strmif/IAMLatency"]
old-location: dshow\iamlatency.htm
tech.root: dshow
ms.assetid: 83384ef6-40d6-4d37-866d-6059dc5d7542
ms.date: 4/26/2023
ms.keywords: IAMLatency, IAMLatency interface [DirectShow], IAMLatency interface [DirectShow],described, IAMLatencyInterface, dshow.iamlatency, strmif/IAMLatency
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
 - IAMLatency
 - strmif/IAMLatency
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
 - IAMLatency
---

# IAMLatency interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IAMLatency</code> interface reports the amount of latency that a filter introduces into the graph. Latency is defined as the time that it takes the filter to process a sample. For a source filter, latency is the filter's maximum buffer size, measured in time. For example, a video capture filter that buffers one frame at 30 frames per second introduces a latency of about 33 milliseconds.

Currently, there is no support for using this interface by itself. A source filter that streams live or real-time data should implement the <a href="/windows/desktop/api/strmif/nn-strmif-iampushsource">IAMPushSource</a> interface, which inherits from this interface.

## -inheritance

The <b>IAMLatency</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMLatency</b> also has these types of members:

