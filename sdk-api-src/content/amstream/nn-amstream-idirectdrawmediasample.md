---
UID: NN:amstream.IDirectDrawMediaSample
title: IDirectDrawMediaSample (amstream.h)
description: The IDirectDrawMediaSample interface provides access to DirectDraw surfaces allocated by the Overlay Mixer filter.The allocator for the Overlay Mixer filter creates samples that expose this interface.
helpviewer_keywords: ["IDirectDrawMediaSample","IDirectDrawMediaSample interface [DirectShow]","IDirectDrawMediaSample interface [DirectShow]","described","IDirectDrawMediaSampleInterface","amstream/IDirectDrawMediaSample","dshow.idirectdrawmediasample"]
old-location: dshow\idirectdrawmediasample.htm
tech.root: dshow
ms.assetid: 0a83b257-e88f-4870-924c-56ddc325f17f
ms.date: 4/26/2023
ms.keywords: IDirectDrawMediaSample, IDirectDrawMediaSample interface [DirectShow], IDirectDrawMediaSample interface [DirectShow],described, IDirectDrawMediaSampleInterface, amstream/IDirectDrawMediaSample, dshow.idirectdrawmediasample
req.header: amstream.h
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
 - IDirectDrawMediaSample
 - amstream/IDirectDrawMediaSample
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
 - IDirectDrawMediaSample
---

# IDirectDrawMediaSample interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IDirectDrawMediaSample</code> interface provides access to DirectDraw surfaces allocated by the <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter.

The allocator for the Overlay Mixer filter creates samples that expose this interface. These samples are used for connections between the Overlay Mixer and upstream decoder filters. Decoder filters can use this interface to unlock the DirectDraw surface while still holding it, so that other components can access the surface.

Samples that support this interface also support the <a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample</a> interface.

The Overlay Mixer's allocator exposes the <a href="/windows/desktop/api/amstream/nn-amstream-idirectdrawmediasampleallocator">IDirectDrawMediaSampleAllocator</a>.

## -inheritance

The <b>IDirectDrawMediaSample</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectDrawMediaSample</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

