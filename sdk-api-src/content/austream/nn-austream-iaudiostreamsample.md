---
UID: NN:austream.IAudioStreamSample
title: IAudioStreamSample (austream.h)
description: Note  This interface is deprecated.
helpviewer_keywords: ["IAudioStreamSample","IAudioStreamSample interface [DirectShow]","IAudioStreamSample interface [DirectShow]","described","IAudioStreamSampleInterface","austream/IAudioStreamSample","dshow.iaudiostreamsample"]
old-location: dshow\iaudiostreamsample.htm
tech.root: dshow
ms.assetid: 53deec43-30ca-472e-9a82-750049686d2a
ms.date: 4/26/2023
ms.keywords: IAudioStreamSample, IAudioStreamSample interface [DirectShow], IAudioStreamSample interface [DirectShow],described, IAudioStreamSampleInterface, austream/IAudioStreamSample, dshow.iaudiostreamsample
req.header: austream.h
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
 - IAudioStreamSample
 - austream/IAudioStreamSample
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - austream.h
api_name:
 - IAudioStreamSample
---

# IAudioStreamSample interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IAudioStreamSample</code> interface retrieves information from the underlying <a href="/windows/desktop/api/austream/nn-austream-iaudiodata">IAudioData</a> data objects.

For sample code that implements the audio streaming interfaces, see <a href="/windows/desktop/DirectShow/multimedia-streaming-sample-code">Multimedia Streaming Sample Code</a>.

Implement this interface on audio stream sample objects when they need access to an <a href="/windows/desktop/api/austream/nn-austream-iaudiodata">IAudioData</a> object's data.

Use this interface when your application needs to access an <a href="/windows/desktop/api/austream/nn-austream-iaudiodata">IAudioData</a> object's data for its audio stream.

## -inheritance

The <b>IAudioStreamSample</b> interface inherits from <a href="/windows/desktop/api/mmstream/nn-mmstream-istreamsample">IStreamSample</a>. <b>IAudioStreamSample</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/mmstream/nn-mmstream-istreamsample">IStreamSample</a>
