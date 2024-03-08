---
UID: NF:ddstream.IDirectDrawMediaStream.GetDirectDraw
title: IDirectDrawMediaStream::GetDirectDraw (ddstream.h)
description: Note  This interface is deprecated. New applications should not use it. Retrieves a pointer to the DirectDraw object used by the current media stream.
helpviewer_keywords: ["GetDirectDraw","GetDirectDraw method [DirectShow]","GetDirectDraw method [DirectShow]","IDirectDrawMediaStream interface","IDirectDrawMediaStream interface [DirectShow]","GetDirectDraw method","IDirectDrawMediaStream.GetDirectDraw","IDirectDrawMediaStream::GetDirectDraw","IDirectDrawMediaStreamGetDirectDraw","ddstream/IDirectDrawMediaStream::GetDirectDraw","dshow.idirectdrawmediastream_getdirectdraw"]
old-location: dshow\idirectdrawmediastream_getdirectdraw.htm
tech.root: dshow
ms.assetid: 44c505fe-70d9-49bd-9135-8a6dc2c72e98
ms.date: 4/26/2023
ms.keywords: GetDirectDraw, GetDirectDraw method [DirectShow], GetDirectDraw method [DirectShow],IDirectDrawMediaStream interface, IDirectDrawMediaStream interface [DirectShow],GetDirectDraw method, IDirectDrawMediaStream.GetDirectDraw, IDirectDrawMediaStream::GetDirectDraw, IDirectDrawMediaStreamGetDirectDraw, ddstream/IDirectDrawMediaStream::GetDirectDraw, dshow.idirectdrawmediastream_getdirectdraw
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
 - IDirectDrawMediaStream::GetDirectDraw
 - ddstream/IDirectDrawMediaStream::GetDirectDraw
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
 - IDirectDrawMediaStream.GetDirectDraw
---

# IDirectDrawMediaStream::GetDirectDraw


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Retrieves a pointer to the DirectDraw object used by the current media stream.

## -parameters

### -param ppDirectDraw [out]

Address of a pointer to an <b>IDirectDraw</b> interface that will contain the current media stream's associated DirectDraw object.

## -returns

Returns S_OK if successful or E_POINTER if the parameter is invalid.

## -remarks

If you haven't initialized the stream yet, the retrieved pointer will be <b>NULL</b> and the method will return S_OK. If you have initialized the stream, this method increments the retrieved pointer's reference count.

## -see-also

<a href="/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream">IDirectDrawMediaStream Interface</a>