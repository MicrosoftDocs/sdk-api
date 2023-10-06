---
UID: NN:mmstream.IMultiMediaStream
title: IMultiMediaStream (mmstream.h)
description: Note  This interface is deprecated.
helpviewer_keywords: ["IMultiMediaStream","IMultiMediaStream interface [DirectShow]","IMultiMediaStream interface [DirectShow]","described","IMultiMediaStreamInterface","dshow.imultimediastream","mmstream/IMultiMediaStream"]
old-location: dshow\imultimediastream.htm
tech.root: dshow
ms.assetid: 8be6c74f-9290-48b4-ad66-8d7d7cc94174
ms.date: 4/26/2023
ms.keywords: IMultiMediaStream, IMultiMediaStream interface [DirectShow], IMultiMediaStream interface [DirectShow],described, IMultiMediaStreamInterface, dshow.imultimediastream, mmstream/IMultiMediaStream
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
 - IMultiMediaStream
 - mmstream/IMultiMediaStream
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
 - IMultiMediaStream
---

# IMultiMediaStream interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IMultiMediaStream</code> interface is exposed by the AMMultimediaStream object. It contains methods for enumerating the media streams, retrieving information about them, and running and stopping them.

## -inheritance

The <b>IMultiMediaStream</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMultiMediaStream</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammultimediastream">IAMMultiMediaStream Interface</a>
