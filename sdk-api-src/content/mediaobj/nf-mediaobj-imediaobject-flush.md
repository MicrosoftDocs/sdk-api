---
UID: NF:mediaobj.IMediaObject.Flush
title: IMediaObject::Flush (mediaobj.h)
description: The Flush method flushes all internally buffered data.
helpviewer_keywords: ["Flush","Flush method [DirectShow]","Flush method [DirectShow]","IMediaObject interface","IMediaObject interface [DirectShow]","Flush method","IMediaObject.Flush","IMediaObject::Flush","IMediaObjectFlush","dshow.imediaobject_flush","mediaobj/IMediaObject::Flush"]
old-location: dshow\imediaobject_flush.htm
tech.root: dshow
ms.assetid: c80001b8-5648-430a-b565-e90486c48ac5
ms.date: 4/26/2023
ms.keywords: Flush, Flush method [DirectShow], Flush method [DirectShow],IMediaObject interface, IMediaObject interface [DirectShow],Flush method, IMediaObject.Flush, IMediaObject::Flush, IMediaObjectFlush, dshow.imediaobject_flush, mediaobj/IMediaObject::Flush
req.header: mediaobj.h
req.include-header: Dmo.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaObject::Flush
 - mediaobj/IMediaObject::Flush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaObject.Flush
---

# IMediaObject::Flush


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Flush</code> method flushes all internally buffered data.



## -returns

Returns S_OK if successful. Otherwise, returns an <b>HRESULT</b> value indicating the cause of the error.

## -remarks

The DMO performs the following actions when this method is called:

<ul>
<li>Releases any <a href="/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer">IMediaBuffer</a> references it holds.</li>
<li>Discards any values that specify the time stamp or sample length for a media buffer.</li>
<li>Reinitializes any internal states that depend on the contents of a media sample.</li>
</ul>
Media types, maximum latency, and locked state do not change.

When the method returns, every input stream accepts data. Output streams cannot produce any data until the application calls the <a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput">IMediaObject::ProcessInput</a> method on at least one input stream.

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject Interface</a>
