---
UID: NN:ddstream.IDirectDrawStreamSample
title: IDirectDrawStreamSample (ddstream.h)
description: Note  This interface is deprecated.
helpviewer_keywords: ["IDirectDrawStreamSample","IDirectDrawStreamSample interface [DirectShow]","IDirectDrawStreamSample interface [DirectShow]","described","IDirectDrawStreamSampleInterface","ddstream/IDirectDrawStreamSample","dshow.idirectdrawstreamsample"]
old-location: dshow\idirectdrawstreamsample.htm
tech.root: dshow
ms.assetid: afc8ac84-4629-4c5d-b4b2-59c1eb1af35d
ms.date: 4/26/2023
ms.keywords: IDirectDrawStreamSample, IDirectDrawStreamSample interface [DirectShow], IDirectDrawStreamSample interface [DirectShow],described, IDirectDrawStreamSampleInterface, ddstream/IDirectDrawStreamSample, dshow.idirectdrawstreamsample
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
 - IDirectDrawStreamSample
 - ddstream/IDirectDrawStreamSample
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
 - IDirectDrawStreamSample
---

# IDirectDrawStreamSample interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IDirectDrawStreamSample</code> interface provides methods that set and retrieve pointers to the Microsoft DirectDraw surface associated with the current stream sample.

This interface isn't intended for implementation by application developers. It is exposed by sample objects created by the DirectDraw stream.

Use this interface when applications need to set clipping rectangles and retrieve the rendering surface for DirectDraw stream samples.

## -inheritance

The <b>IDirectDrawStreamSample</b> interface inherits from <a href="/windows/desktop/api/mmstream/nn-mmstream-istreamsample">IStreamSample</a>. <b>IDirectDrawStreamSample</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/mmstream/nn-mmstream-istreamsample">IStreamSample</a>
