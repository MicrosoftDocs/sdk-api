---
UID: NN:strmif.IMediaSample2
title: IMediaSample2 (strmif.h)
description: The IMediaSample2 interface sets and retrieves properties on media samples.This interface inherits the IMediaSample interface.
helpviewer_keywords: ["IMediaSample2","IMediaSample2 interface [DirectShow]","IMediaSample2 interface [DirectShow]","described","IMediaSample2Interface","dshow.imediasample2","strmif/IMediaSample2"]
old-location: dshow\imediasample2.htm
tech.root: dshow
ms.assetid: 638cb75d-9be6-4ba1-a116-47e2d62b689d
ms.date: 4/26/2023
ms.keywords: IMediaSample2, IMediaSample2 interface [DirectShow], IMediaSample2 interface [DirectShow],described, IMediaSample2Interface, dshow.imediasample2, strmif/IMediaSample2
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
 - IMediaSample2
 - strmif/IMediaSample2
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
 - IMediaSample2
---

# IMediaSample2 interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IMediaSample2</code> interface sets and retrieves properties on media samples.

This interface inherits the <a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample</a> interface. Whereas the <b>IMediaSample</b> interface requires separate method calls for each sample property, the <code>IMediaSample2</code> interface has methods for setting and retrieving multiple properties at once.

Media samples are not guaranteed to support <code>IMediaSample2</code>. However, if an allocator creates samples that support <code>IMediaSample2</code>, all of the samples that it creates must support the interface. For any given media sample, the <b>IMediaSample2::GetProperties</b> method returns the same values as the individual <b>IMediaSample</b> methods. Therefore, you can use whichever version you prefer.

## -inheritance

The <b>IMediaSample2</b> interface inherits from <a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample</a>. <b>IMediaSample2</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample</a>
