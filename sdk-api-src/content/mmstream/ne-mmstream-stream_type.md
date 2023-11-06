---
UID: NE:mmstream.__MIDL___MIDL_itf_mmstream_0000_0000_0001
title: STREAM_TYPE (mmstream.h)
description: Note  This API is deprecated. New applications should not use it. Defines the direction of data flow for the stream.
helpviewer_keywords: ["STREAMTYPE_READ","STREAMTYPE_TRANSFORM","STREAMTYPE_WRITE","STREAM_TYPE","STREAM_TYPE enumeration [DirectShow]","dshow.stream_type","mmstream/STREAMTYPE_READ","mmstream/STREAMTYPE_TRANSFORM","mmstream/STREAMTYPE_WRITE","mmstream/STREAM_TYPE"]
old-location: dshow\stream_type.htm
tech.root: dshow
ms.assetid: 07ab5ded-28b8-4cac-b4da-76f07ad351ef
ms.date: 4/26/2023
ms.keywords: STREAMTYPE_READ, STREAMTYPE_TRANSFORM, STREAMTYPE_WRITE, STREAM_TYPE, STREAM_TYPE enumeration [DirectShow], dshow.stream_type, mmstream/STREAMTYPE_READ, mmstream/STREAMTYPE_TRANSFORM, mmstream/STREAMTYPE_WRITE, mmstream/STREAM_TYPE
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
req.typenames: STREAM_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_mmstream_0000_0000_0001
 - mmstream/__MIDL___MIDL_itf_mmstream_0000_0000_0001
 - STREAM_TYPE
 - mmstream/STREAM_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmstream.h
api_name:
 - STREAM_TYPE
---

# STREAM_TYPE enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This API is deprecated. New applications should not use it.</div>
<div> </div>
Defines the direction of data flow for the stream.

## -enum-fields

### -field STREAMTYPE_READ:0

Application can read the stream.

### -field STREAMTYPE_WRITE:1

Application can write to the stream.

### -field STREAMTYPE_TRANSFORM:2

Application reads and writes to the stream.

## -remarks

Transform streams are read/write where the sample is updated in place.

## -see-also

<a href="/windows/desktop/DirectShow/multimedia-streaming-types">Multimedia Streaming Enumeration Types</a>
