---
UID: NF:segment.IMSVidStreamBufferSourceEvent3.ContentPrimarilyAudio
title: IMSVidStreamBufferSourceEvent3::ContentPrimarilyAudio (segment.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["ContentPrimarilyAudio","ContentPrimarilyAudio method [Microsoft TV Technologies]","ContentPrimarilyAudio method [Microsoft TV Technologies]","IMSVidStreamBufferSourceEvent3 interface","IMSVidStreamBufferSourceEvent3 interface [Microsoft TV Technologies]","ContentPrimarilyAudio method","IMSVidStreamBufferSourceEvent3.ContentPrimarilyAudio","IMSVidStreamBufferSourceEvent3::ContentPrimarilyAudio","IMSVidStreamBufferSourceEvent3ContentPrimarilyAudio","mstv.imsvidstreambuffersourceevent3_contentprimarilyaudio","segment/IMSVidStreamBufferSourceEvent3::ContentPrimarilyAudio"]
old-location: mstv\imsvidstreambuffersourceevent3_contentprimarilyaudio.htm
tech.root: mstv
ms.assetid: 5ee38fac-78f8-4130-8d16-db5380e11c5f
ms.date: 12/05/2018
ms.keywords: ContentPrimarilyAudio, ContentPrimarilyAudio method [Microsoft TV Technologies], ContentPrimarilyAudio method [Microsoft TV Technologies],IMSVidStreamBufferSourceEvent3 interface, IMSVidStreamBufferSourceEvent3 interface [Microsoft TV Technologies],ContentPrimarilyAudio method, IMSVidStreamBufferSourceEvent3.ContentPrimarilyAudio, IMSVidStreamBufferSourceEvent3::ContentPrimarilyAudio, IMSVidStreamBufferSourceEvent3ContentPrimarilyAudio, mstv.imsvidstreambuffersourceevent3_contentprimarilyaudio, segment/IMSVidStreamBufferSourceEvent3::ContentPrimarilyAudio
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IMSVidStreamBufferSourceEvent3::ContentPrimarilyAudio
 - segment/IMSVidStreamBufferSourceEvent3::ContentPrimarilyAudio
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
 - IMSVidStreamBufferSourceEvent3.ContentPrimarilyAudio
---

# IMSVidStreamBufferSourceEvent3::ContentPrimarilyAudio


## -description

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>ContentPrimarilyAudio</b> method is called when the Stream Buffer Engine is processing primarily audio data.

## -parameters

## -returns

Return S_OK or an error code.

## -remarks

This event is sent when the <a href="/previous-versions/windows/desktop/legacy/dd695136(v=vs.85)">MSVidStreamBufferSource</a> object receives an STREAMBUFFER_EC_PRIMARY_AUDIO event from the Stream Buffer Engine. For more information, see <a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-codes">Stream Buffer Engine Event Codes</a>.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambuffersourceevent3">IMSVidStreamBufferSourceEvent3 Interface</a>