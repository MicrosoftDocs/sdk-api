---
UID: NN:ddstream.IDirectDrawMediaStream
title: IDirectDrawMediaStream (ddstream.h)
description: Note  This interface is deprecated.
helpviewer_keywords: ["IDirectDrawMediaStream","IDirectDrawMediaStream interface [DirectShow]","IDirectDrawMediaStream interface [DirectShow]","described","IDirectDrawMediaStreamInterface","ddstream/IDirectDrawMediaStream","dshow.idirectdrawmediastream"]
old-location: dshow\idirectdrawmediastream.htm
tech.root: dshow
ms.assetid: 858af0c3-9e22-45d8-ab08-307eb39a8977
ms.date: 4/26/2023
ms.keywords: IDirectDrawMediaStream, IDirectDrawMediaStream interface [DirectShow], IDirectDrawMediaStream interface [DirectShow],described, IDirectDrawMediaStreamInterface, ddstream/IDirectDrawMediaStream, dshow.idirectdrawmediastream
req.header: ddstream.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectDrawMediaStream
 - ddstream/IDirectDrawMediaStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ddstream.h
api_name:
 - IDirectDrawMediaStream
---

# IDirectDrawMediaStream interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IDirectDrawMediaStream</code> interface controls media streams that appear on Microsoft DirectDraw surfaces. To stream to a DirectDraw surface, DirectDraw must support the video stream format.

For sample code that implements the multimedia streaming interfaces, see <a href="/windows/desktop/DirectShow/multimedia-streaming-sample-code">Multimedia Streaming Sample Code</a>.

This interface isn't intended for implementation by application developers. It is exposed on DirectDraw media streams that can be added to a DirectShow multimedia stream.

Use this interface when you want to send a video stream to a DirectDraw surface.

## -inheritance

The <b>IDirectDrawMediaStream</b> interface inherits from <a href="/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream</a>. <b>IDirectDrawMediaStream</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream</a>
