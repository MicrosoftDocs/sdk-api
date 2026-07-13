---
UID: NS:strmif.CodecAPIEventData
title: CodecAPIEventData (strmif.h)
description: The CodecAPIEventData structure (strmif.h) contains event data for the EC_CODECAPI_EVENT event. This event is sent by codecs that support the ICodecAPI interface.
helpviewer_keywords: ["CodecAPIEventData","CodecAPIEventData structure [DirectShow]","CodecAPIEventDataStructure","dshow.codecapieventdata","strmif/CodecAPIEventData"]
old-location: dshow\codecapieventdata.htm
tech.root: dshow
ms.assetid: 04d0177d-ec9d-4f23-abd1-a37c787c24b2
ms.date: 4/26/2023
ms.keywords: CodecAPIEventData, CodecAPIEventData structure [DirectShow], CodecAPIEventDataStructure, dshow.codecapieventdata, strmif/CodecAPIEventData
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps \| UWP apps]
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
 - CodecAPIEventData
 - strmif/CodecAPIEventData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - CodecAPIEventData
---

# CodecAPIEventData structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>CodecAPIEventData</b> structure contains event data for the <a href="/windows/desktop/DirectShow/ec-codecapi-event">EC_CODECAPI_EVENT</a> event. This event is sent by codecs that support the <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a> interface.

## -struct-fields

### -field guid

A GUID that identifies the codec event.

### -field dataLength

The length of the additional data that follows this structure, in bytes.
          The value can be zero.

### -field reserved

Reserved; do not use.

## -remarks

This structure may be followed by addition data, depending on the codec event. For more information, see <a href="/windows/desktop/api/strmif/nf-strmif-icodecapi-registerforevent">ICodecAPI::RegisterForEvent</a>.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/api/strmif/nf-strmif-icodecapi-registerforevent">ICodecAPI::RegisterForEvent</a>
