---
UID: NF:ddstream.IDirectDrawMediaStream.GetTimePerFrame
title: IDirectDrawMediaStream::GetTimePerFrame (ddstream.h)
description: Note  This interface is deprecated. New applications should not use it. Retrieves the average frames per second from a video stream.
helpviewer_keywords: ["GetTimePerFrame","GetTimePerFrame method [DirectShow]","GetTimePerFrame method [DirectShow]","IDirectDrawMediaStream interface","IDirectDrawMediaStream interface [DirectShow]","GetTimePerFrame method","IDirectDrawMediaStream.GetTimePerFrame","IDirectDrawMediaStream::GetTimePerFrame","IDirectDrawMediaStreamGetTimePerFrame","ddstream/IDirectDrawMediaStream::GetTimePerFrame","dshow.idirectdrawmediastream_gettimeperframe"]
old-location: dshow\idirectdrawmediastream_gettimeperframe.htm
tech.root: dshow
ms.assetid: 24133185-0d5f-41fc-b381-ef982db46dd1
ms.date: 12/05/2018
ms.keywords: GetTimePerFrame, GetTimePerFrame method [DirectShow], GetTimePerFrame method [DirectShow],IDirectDrawMediaStream interface, IDirectDrawMediaStream interface [DirectShow],GetTimePerFrame method, IDirectDrawMediaStream.GetTimePerFrame, IDirectDrawMediaStream::GetTimePerFrame, IDirectDrawMediaStreamGetTimePerFrame, ddstream/IDirectDrawMediaStream::GetTimePerFrame, dshow.idirectdrawmediastream_gettimeperframe
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
 - IDirectDrawMediaStream::GetTimePerFrame
 - ddstream/IDirectDrawMediaStream::GetTimePerFrame
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
 - IDirectDrawMediaStream.GetTimePerFrame
---

# IDirectDrawMediaStream::GetTimePerFrame


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Retrieves the average frames per second from a video stream.

## -parameters

### -param pFrameTime [out]

Pointer to a <b>STREAM_TIME</b> value that indicates the average time per frame in 100-nanosecond units. (See <a href="/windows/desktop/DirectShow/multimedia-streaming-data-types">Multimedia Streaming Data Types</a>.)

## -returns

Returns S_OK if successful or E_POINTER if the pointer is invalid.

## -see-also

<a href="/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream">IDirectDrawMediaStream Interface</a>