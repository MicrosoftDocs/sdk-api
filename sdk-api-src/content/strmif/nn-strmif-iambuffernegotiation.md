---
UID: NN:strmif.IAMBufferNegotiation
title: IAMBufferNegotiation (strmif.h)
description: The IAMBufferNegotiation interface requests the number of buffers for a filter to create and size of each buffer.
helpviewer_keywords: ["IAMBufferNegotiation","IAMBufferNegotiation interface [DirectShow]","IAMBufferNegotiation interface [DirectShow]","described","IAMBufferNegotiationInterface","dshow.iambuffernegotiation","strmif/IAMBufferNegotiation"]
old-location: dshow\iambuffernegotiation.htm
tech.root: dshow
ms.assetid: 68e98afd-3275-49bb-b165-48ed40026e76
ms.date: 4/26/2023
ms.keywords: IAMBufferNegotiation, IAMBufferNegotiation interface [DirectShow], IAMBufferNegotiation interface [DirectShow],described, IAMBufferNegotiationInterface, dshow.iambuffernegotiation, strmif/IAMBufferNegotiation
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
 - IAMBufferNegotiation
 - strmif/IAMBufferNegotiation
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
 - IAMBufferNegotiation
---

# IAMBufferNegotiation interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IAMBufferNegotiation</code> interface requests the number of buffers for a filter to create and size of each buffer. This interface can be exposed by any pin that connects using the <a href="/windows/desktop/api/strmif/nn-strmif-imeminputpin">IMemInputPin</a> pin interface, but is typically exposed on the output pins of capture filters.

When two pins connect through <b>IMemInputPin</b>, they agree on an allocator object that is responsible for creating buffers. Normally this process is transparent to the application, but in some situations the application needs more control. If a pin exposes <code>IAMBufferNegotiation</code>, the application can suggest how many buffers to create, the size of the buffers, and other properties. If your application performs preview of captured audio, you can specify a smaller buffer size to reduce latency. Teleconferencing applications should specify a minimal number of buffers.

To use this interface, call the <b>SuggestAllocatorProperties</b> method before the pins connect. After the pins connect, call the <b>GetAllocatorProperties</b> method to determine whether the pin honored the request.

<b>Filter developers</b>: Capture filters should always support this interface when possible.

## -inheritance

The <b>IAMBufferNegotiation</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMBufferNegotiation</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
