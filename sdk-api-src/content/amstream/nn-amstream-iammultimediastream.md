---
UID: NN:amstream.IAMMultiMediaStream
title: IAMMultiMediaStream (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The IAMMultiMediaStream interface is supported by the multimedia stream object. It contains methods for creating the underlying filter graph that the object manages.
helpviewer_keywords: ["IAMMultiMediaStream","IAMMultiMediaStream interface [DirectShow]","IAMMultiMediaStream interface [DirectShow]","described","IAMMultiMediaStreamInterface","amstream/IAMMultiMediaStream","dshow.iammultimediastream"]
old-location: dshow\iammultimediastream.htm
tech.root: dshow
ms.assetid: 2f604156-68ef-4770-9929-6dbfd46c4d6d
ms.date: 4/26/2023
ms.keywords: IAMMultiMediaStream, IAMMultiMediaStream interface [DirectShow], IAMMultiMediaStream interface [DirectShow],described, IAMMultiMediaStreamInterface, amstream/IAMMultiMediaStream, dshow.iammultimediastream
req.header: amstream.h
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
 - IAMMultiMediaStream
 - amstream/IAMMultiMediaStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amstream.h
api_name:
 - IAMMultiMediaStream
---

# IAMMultiMediaStream interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IAMMultiMediaStream</code> interface is supported by the multimedia stream object. It contains methods for creating the underlying filter graph that the object manages.

## -inheritance

The <b>IAMMultiMediaStream</b> interface inherits from <a href="/windows/desktop/api/mmstream/nn-mmstream-imultimediastream">IMultiMediaStream</a>. <b>IAMMultiMediaStream</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/mmstream/nn-mmstream-imultimediastream">IMultiMediaStream</a>
