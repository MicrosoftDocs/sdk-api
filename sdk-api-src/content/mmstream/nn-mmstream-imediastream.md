---
UID: NN:mmstream.IMediaStream
title: IMediaStream (mmstream.h)
description: Note  This interface is deprecated.
helpviewer_keywords: ["IMediaStream","IMediaStream interface [DirectShow]","IMediaStream interface [DirectShow]","described","IMediaStreamInterface","dshow.imediastream","mmstream/IMediaStream"]
old-location: dshow\imediastream.htm
tech.root: dshow
ms.assetid: 97f5dfdc-5941-4b58-a618-1c7e9f6665e1
ms.date: 4/26/2023
ms.keywords: IMediaStream, IMediaStream interface [DirectShow], IMediaStream interface [DirectShow],described, IMediaStreamInterface, dshow.imediastream, mmstream/IMediaStream
req.header: mmstream.h
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
 - IMediaStream
 - mmstream/IMediaStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mmstream.h
api_name:
 - IMediaStream
---

# IMediaStream interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <b>IMediaStream</b> interface provides access to the characteristics of a media stream, such as the stream's media type and purpose ID. It also has methods that create data samples.

For sample code that implements the multimedia streaming interfaces, see <a href="/windows/desktop/DirectShow/multimedia-streaming-sample-code">Multimedia Streaming Sample Code</a>.

Implement this interface when you want to add media type-specific functionality to your media stream. This interface is implemented on multimedia stream objects. <b>IMediaStream</b> provides generic sample-creation methods, but you usually want to write a more powerful version of these methods that will take advantage of your media type's specific characteristics.

Use this interface when your application needs to access a stream's media type information and create data samples.

## -inheritance

The <b>IMediaStream</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMediaStream</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

