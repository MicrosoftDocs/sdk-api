---
UID: NF:ddstream.IDirectDrawMediaStream.SetDirectDraw
title: IDirectDrawMediaStream::SetDirectDraw (ddstream.h)
description: Note  This interface is deprecated. New applications should not use it. Sets the current media stream's DirectDraw object.
helpviewer_keywords: ["IDirectDrawMediaStream interface [DirectShow]","SetDirectDraw method","IDirectDrawMediaStream.SetDirectDraw","IDirectDrawMediaStream::SetDirectDraw","IDirectDrawMediaStreamSetDirectDraw","SetDirectDraw","SetDirectDraw method [DirectShow]","SetDirectDraw method [DirectShow]","IDirectDrawMediaStream interface","ddstream/IDirectDrawMediaStream::SetDirectDraw","dshow.idirectdrawmediastream_setdirectdraw"]
old-location: dshow\idirectdrawmediastream_setdirectdraw.htm
tech.root: dshow
ms.assetid: ffa425c5-5f81-4963-bf23-2139d8b245b3
ms.date: 4/26/2023
ms.keywords: IDirectDrawMediaStream interface [DirectShow],SetDirectDraw method, IDirectDrawMediaStream.SetDirectDraw, IDirectDrawMediaStream::SetDirectDraw, IDirectDrawMediaStreamSetDirectDraw, SetDirectDraw, SetDirectDraw method [DirectShow], SetDirectDraw method [DirectShow],IDirectDrawMediaStream interface, ddstream/IDirectDrawMediaStream::SetDirectDraw, dshow.idirectdrawmediastream_setdirectdraw
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
 - IDirectDrawMediaStream::SetDirectDraw
 - ddstream/IDirectDrawMediaStream::SetDirectDraw
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
 - IDirectDrawMediaStream.SetDirectDraw
---

# IDirectDrawMediaStream::SetDirectDraw


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Sets the current media stream's DirectDraw object.

## -parameters

### -param pDirectDraw [in]

Pointer to an <b>IDirectDraw</b> interface that contains the media stream's new DirectDraw object.

## -returns

Returns S_OK if successful or E_POINTER if the pointer is invalid.

## -remarks

This method fails if the current stream already has allocated samples and its DirectDraw object differs from the specified one. It will always succeed if the specified DirectDraw object matches the stream's current object.

If this stream has no allocated samples, you can set <i>pDirectDraw</i> to <b>NULL</b>. This forces the stream to release its reference to the current DirectDraw object.

## -see-also

<a href="/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream">IDirectDrawMediaStream Interface</a>