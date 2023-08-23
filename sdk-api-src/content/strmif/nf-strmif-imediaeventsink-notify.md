---
UID: NF:strmif.IMediaEventSink.Notify
title: IMediaEventSink::Notify (strmif.h)
description: The Notify method notifies the Filter Graph Manager of an event.
helpviewer_keywords: ["IMediaEventSink interface [DirectShow]","Notify method","IMediaEventSink.Notify","IMediaEventSink::Notify","IMediaEventSinkNotify","Notify","Notify method [DirectShow]","Notify method [DirectShow]","IMediaEventSink interface","dshow.imediaeventsink_notify","strmif/IMediaEventSink::Notify"]
old-location: dshow\imediaeventsink_notify.htm
tech.root: dshow
ms.assetid: 331f8d58-c7c6-40dd-88ca-5678c7b8c8f1
ms.date: 4/26/2023
ms.keywords: IMediaEventSink interface [DirectShow],Notify method, IMediaEventSink.Notify, IMediaEventSink::Notify, IMediaEventSinkNotify, Notify, Notify method [DirectShow], Notify method [DirectShow],IMediaEventSink interface, dshow.imediaeventsink_notify, strmif/IMediaEventSink::Notify
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
 - IMediaEventSink::Notify
 - strmif/IMediaEventSink::Notify
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
 - IMediaEventSink.Notify
---

# IMediaEventSink::Notify


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Notify</code> method notifies the Filter Graph Manager of an event.

## -parameters

### -param EventCode [in]

Identifier of the event.

### -param EventParam1 [in]

First event parameter.

### -param EventParam2 [in]

Second event parameter.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

The event is queued but not delivered to the application on this thread. For a list of notification codes and event parameter values, see <a href="/windows/desktop/DirectShow/event-notification-codes">Event Notification Codes</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediaeventsink">IMediaEventSink Interface</a>