---
UID: NF:austream.IAudioMediaStream.GetFormat
title: IAudioMediaStream::GetFormat (austream.h)
description: Note  This interface is deprecated. New applications should not use it. Retrieves the stream data's current format.
helpviewer_keywords: ["GetFormat","GetFormat method [DirectShow]","GetFormat method [DirectShow]","IAudioMediaStream interface","IAudioMediaStream interface [DirectShow]","GetFormat method","IAudioMediaStream.GetFormat","IAudioMediaStream::GetFormat","IAudioMediaStreamGetFormat","austream/IAudioMediaStream::GetFormat","dshow.iaudiomediastream_getformat"]
old-location: dshow\iaudiomediastream_getformat.htm
tech.root: dshow
ms.assetid: df582b90-f537-42cf-a83e-109a20446d8a
ms.date: 4/26/2023
ms.keywords: GetFormat, GetFormat method [DirectShow], GetFormat method [DirectShow],IAudioMediaStream interface, IAudioMediaStream interface [DirectShow],GetFormat method, IAudioMediaStream.GetFormat, IAudioMediaStream::GetFormat, IAudioMediaStreamGetFormat, austream/IAudioMediaStream::GetFormat, dshow.iaudiomediastream_getformat
req.header: austream.h
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
 - IAudioMediaStream::GetFormat
 - austream/IAudioMediaStream::GetFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - austream.h
api_name:
 - IAudioMediaStream.GetFormat
---

# IAudioMediaStream::GetFormat


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Retrieves the stream data's current format.

## -parameters

### -param pWaveFormatCurrent [out]

Pointer to a <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure that contains the stream data's current format.

## -returns

Returns S_OK if successful or E_POINTER if the required parameter is <b>NULL</b>.

## -remarks

Currently, Microsoft DirectShow supports only PCM wave data.

## -see-also

<a href="/windows/desktop/api/austream/nn-austream-iaudiomediastream">IAudioMediaStream Interface</a>