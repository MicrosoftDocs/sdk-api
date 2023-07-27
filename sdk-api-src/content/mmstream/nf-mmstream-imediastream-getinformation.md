---
UID: NF:mmstream.IMediaStream.GetInformation
title: IMediaStream::GetInformation (mmstream.h)
description: Note  This interface is deprecated. New applications should not use it. Retrieves the stream's purpose ID and media type.
helpviewer_keywords: ["GetInformation","GetInformation method [DirectShow]","GetInformation method [DirectShow]","IMediaStream interface","IMediaStream interface [DirectShow]","GetInformation method","IMediaStream.GetInformation","IMediaStream::GetInformation","IMediaStreamGetInformation","dshow.imediastream_getinformation","mmstream/IMediaStream::GetInformation"]
old-location: dshow\imediastream_getinformation.htm
tech.root: dshow
ms.assetid: e4ecae45-e2bf-44dd-8901-0892c02d708c
ms.date: 4/26/2023
ms.keywords: GetInformation, GetInformation method [DirectShow], GetInformation method [DirectShow],IMediaStream interface, IMediaStream interface [DirectShow],GetInformation method, IMediaStream.GetInformation, IMediaStream::GetInformation, IMediaStreamGetInformation, dshow.imediastream_getinformation, mmstream/IMediaStream::GetInformation
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
 - IMediaStream::GetInformation
 - mmstream/IMediaStream::GetInformation
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
 - IMediaStream.GetInformation
---

# IMediaStream::GetInformation


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Retrieves the stream's purpose ID and media type.

## -parameters

### -param pPurposeId [out]

Pointer to an <b>MSPID</b> value that will contain the stream's purpose ID (see <a href="/windows/desktop/DirectShow/multimedia-streaming-data-types">Multimedia Streaming Data Types</a>). If this parameter is <b>NULL</b> on entry, the method won't retrieve the purpose ID.

### -param pType [out]

Pointer to a <a href="/previous-versions/windows/desktop/api/mmstream/ne-mmstream-stream_type">STREAM_TYPE</a> enumerated data type value that will contain the stream's media type. If this parameter is <b>NULL</b> on entry, the method won't retrieve the media type.

## -returns

Returns S_OK if successful or E_POINTER if one of the parameters is invalid.

## -remarks

The value retrieved in the <i>pPurposeId</i> parameter will usually be either MSPID_PrimaryVideo, which identifies the primary video stream, or MSPID_PrimaryAudio, which identifies the primary audio stream; however, you can define other values if necessary.

## -see-also

<a href="/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream Interface</a>