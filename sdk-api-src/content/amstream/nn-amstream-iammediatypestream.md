---
UID: NN:amstream.IAMMediaTypeStream
title: IAMMediaTypeStream (amstream.h)
description: Note  This interface is deprecated.
helpviewer_keywords: ["IAMMediaTypeStream","IAMMediaTypeStream interface [DirectShow]","IAMMediaTypeStream interface [DirectShow]","described","IAMMediaTypeStreamInterface","amstream/IAMMediaTypeStream","dshow.iammediatypestream"]
old-location: dshow\iammediatypestream.htm
tech.root: dshow
ms.assetid: 6ca1bad2-625b-4415-8311-acd5443452c1
ms.date: 4/26/2023
ms.keywords: IAMMediaTypeStream, IAMMediaTypeStream interface [DirectShow], IAMMediaTypeStream interface [DirectShow],described, IAMMediaTypeStreamInterface, amstream/IAMMediaTypeStream, dshow.iammediatypestream
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
 - IAMMediaTypeStream
 - amstream/IAMMediaTypeStream
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
 - IAMMediaTypeStream
---

# IAMMediaTypeStream interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
This interface contains methods for creating multimedia streams with arbitrary media types. Use this interface if you need to create a multimedia stream with a format that is not supported by the other Microsoft DirectShow multimedia streaming interfaces.

<div class="alert"><b>Note</b>  For video streams, use the <a href="/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream">IDirectDrawMediaStream</a> interface instead of this interface. For audio streams, use the <a href="/windows/desktop/api/austream/nn-austream-iaudiomediastream">IAudioMediaStream</a> interface.</div>
<div> </div>

## -inheritance

The <b>IAMMediaTypeStream</b> interface inherits from <a href="/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream</a>. <b>IAMMediaTypeStream</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream</a>
