---
UID: NF:segment.IMSVidStreamBufferV2SourceEvent.ContentPrimarilyAudio
title: IMSVidStreamBufferV2SourceEvent::ContentPrimarilyAudio (segment.h)
description: Fired when an SBE2 source filter receives a STREAMBUFFER_EC_PRIMARY_AUDIO event, which is fired through the IMSVidStreamBufferSourceEvent3 interface, and indicates that SBE is processing primarily audio data.
helpviewer_keywords: ["ContentPrimarilyAudio","ContentPrimarilyAudio method [Microsoft TV Technologies]","ContentPrimarilyAudio method [Microsoft TV Technologies]","IMSVidStreamBufferV2SourceEvent interface","IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies]","ContentPrimarilyAudio method","IMSVidStreamBufferV2SourceEvent.ContentPrimarilyAudio","IMSVidStreamBufferV2SourceEvent::ContentPrimarilyAudio","mstv.imsvidstreambufferv2sourceevent_contentprimarilyaudio","segment/IMSVidStreamBufferV2SourceEvent::ContentPrimarilyAudio"]
old-location: mstv\imsvidstreambufferv2sourceevent_contentprimarilyaudio.htm
tech.root: mstv
ms.assetid: 9056bed3-b4da-4eca-a573-0d9bda3d2127
ms.date: 12/05/2018
ms.keywords: ContentPrimarilyAudio, ContentPrimarilyAudio method [Microsoft TV Technologies], ContentPrimarilyAudio method [Microsoft TV Technologies],IMSVidStreamBufferV2SourceEvent interface, IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies],ContentPrimarilyAudio method, IMSVidStreamBufferV2SourceEvent.ContentPrimarilyAudio, IMSVidStreamBufferV2SourceEvent::ContentPrimarilyAudio, mstv.imsvidstreambufferv2sourceevent_contentprimarilyaudio, segment/IMSVidStreamBufferV2SourceEvent::ContentPrimarilyAudio
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - IMSVidStreamBufferV2SourceEvent::ContentPrimarilyAudio
 - segment/IMSVidStreamBufferV2SourceEvent::ContentPrimarilyAudio
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidStreamBufferV2SourceEvent.ContentPrimarilyAudio
---

# IMSVidStreamBufferV2SourceEvent::ContentPrimarilyAudio


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Fired when an SBE2 source filter receives a <b>STREAMBUFFER_EC_PRIMARY_AUDIO</b> event, which is fired through the <a href="/windows/desktop/api/segment/nn-segment-imsvidstreambuffersourceevent3">IMSVidStreamBufferSourceEvent3</a> interface, and indicates that SBE is processing primarily audio data.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A STREAMBUFFER_EC_PRIMARY_AUDIO event is sent if video samples are captured at a low frame rate. This event generally occurs with audio services on a DVB stream, but it might also indicate a problem with capturing or encoding the video. 

This event applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambufferv2sourceevent">IMSVidStreamBufferV2SourceEvent</a>



<a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-codes">Stream Buffer Engine Event Codes</a>
