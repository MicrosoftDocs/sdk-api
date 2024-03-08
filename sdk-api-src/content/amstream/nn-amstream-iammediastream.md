---
UID: NN:amstream.IAMMediaStream
title: IAMMediaStream (amstream.h)
description: Note  This interface is deprecated.
helpviewer_keywords: ["IAMMediaStream","IAMMediaStream interface [DirectShow]","IAMMediaStream interface [DirectShow]","described","IAMMediaStreamInterface","amstream/IAMMediaStream","dshow.iammediastream"]
old-location: dshow\iammediastream.htm
tech.root: dshow
ms.assetid: 14185e7d-d08d-4fd8-a255-075eaf12a708
ms.date: 4/26/2023
ms.keywords: IAMMediaStream, IAMMediaStream interface [DirectShow], IAMMediaStream interface [DirectShow],described, IAMMediaStreamInterface, amstream/IAMMediaStream, dshow.iammediastream
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
 - IAMMediaStream
 - amstream/IAMMediaStream
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
 - IAMMediaStream
---

# IAMMediaStream interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IAMMediaStream</code> interface handles the internal connections between Microsoft DirectShow filters and filter graphs in applications that use multimedia streaming. This enables applications to automatically negotiate the transfer and conversion of data from the source to the application without having to write code to handle the connection, transfer of data, data conversion, and actual data rendering or file storage. This provides a uniform and predictable method of data access and control.

This interface isn't intended for implementation or use by application developers.

## -inheritance

The <b>IAMMediaStream</b> interface inherits from <a href="/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream</a>. <b>IAMMediaStream</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream</a>
