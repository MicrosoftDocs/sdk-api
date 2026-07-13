---
UID: NF:mmstream.IMediaStream.SendEndOfStream
title: IMediaStream::SendEndOfStream (mmstream.h)
description: Note  This interface is deprecated. New applications should not use it. Forces the current stream to end. If the current stream isn't writable, this method does nothing.
helpviewer_keywords: ["IMediaStream interface [DirectShow]","SendEndOfStream method","IMediaStream.SendEndOfStream","IMediaStream::SendEndOfStream","IMediaStreamSendEndOfStream","SendEndOfStream","SendEndOfStream method [DirectShow]","SendEndOfStream method [DirectShow]","IMediaStream interface","dshow.imediastream_sendendofstream","mmstream/IMediaStream::SendEndOfStream"]
old-location: dshow\imediastream_sendendofstream.htm
tech.root: dshow
ms.assetid: aa774875-1cf2-4792-a492-fef64571ae8f
ms.date: 4/26/2023
ms.keywords: IMediaStream interface [DirectShow],SendEndOfStream method, IMediaStream.SendEndOfStream, IMediaStream::SendEndOfStream, IMediaStreamSendEndOfStream, SendEndOfStream, SendEndOfStream method [DirectShow], SendEndOfStream method [DirectShow],IMediaStream interface, dshow.imediastream_sendendofstream, mmstream/IMediaStream::SendEndOfStream
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
 - IMediaStream::SendEndOfStream
 - mmstream/IMediaStream::SendEndOfStream
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
 - IMediaStream.SendEndOfStream
---

# IMediaStream::SendEndOfStream


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Forces the current stream to end. If the current stream isn't writable, this method does nothing.

## -parameters

### -param dwFlags [in]

Reserved for flag data. Must be zero.

## -returns

Returns S_OK if successful or MS_E_INCOMPATIBLE if the existing sample isn't compatible with the current media stream.

## -remarks

Applications do not call this internal method.

## -see-also

<a href="/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream Interface</a>