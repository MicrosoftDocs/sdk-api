---
UID: NN:mmstream.IStreamSample
title: IStreamSample (mmstream.h)
description: Note  This interface is deprecated.
helpviewer_keywords: ["IStreamSample","IStreamSample interface [DirectShow]","IStreamSample interface [DirectShow]","described","IStreamSampleInterface","dshow.istreamsample","mmstream/IStreamSample"]
old-location: dshow\istreamsample.htm
tech.root: dshow
ms.assetid: 57818d7d-3290-46f7-a3fd-8585cdd64ec3
ms.date: 4/26/2023
ms.keywords: IStreamSample, IStreamSample interface [DirectShow], IStreamSample interface [DirectShow],described, IStreamSampleInterface, dshow.istreamsample, mmstream/IStreamSample
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
 - IStreamSample
 - mmstream/IStreamSample
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
 - IStreamSample
---

# IStreamSample interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IStreamSample</code> interface provides control over the behavior of stream samples. You can retrieve the media stream that created the sample, set or retrieve sample start and stop times, check the sample's completion status, and perform a developer-specified function on the sample itself.

Implement this interface when you implement a media stream for a new media type. The interface is exposed on sample objects created by media streams.

Use this interface when you want to control data samples created by <a href="/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream</a> or its derived interfaces.

In addition to the methods inherited from <b>IUnknown</b>, the <code>IStreamSample</code> interface exposes the following methods.

## -inheritance

The <b>IStreamSample</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStreamSample</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

