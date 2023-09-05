---
UID: NF:segment.IMSVidStreamBufferV2SourceEvent.TimeHole
title: IMSVidStreamBufferV2SourceEvent::TimeHole (segment.h)
description: Fired when the SBE2 source filter receives a STREAMBUFFER_EC_TIMEHOLE event, which indicates playback has reached a gap in recorded content.
helpviewer_keywords: ["IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies]","TimeHole method","IMSVidStreamBufferV2SourceEvent.TimeHole","IMSVidStreamBufferV2SourceEvent::TimeHole","TimeHole","TimeHole method [Microsoft TV Technologies]","TimeHole method [Microsoft TV Technologies]","IMSVidStreamBufferV2SourceEvent interface","mstv.imsvidstreambufferv2sourceevent_timehole","segment/IMSVidStreamBufferV2SourceEvent::TimeHole"]
old-location: mstv\imsvidstreambufferv2sourceevent_timehole.htm
tech.root: mstv
ms.assetid: 2eceda3b-b3d6-4714-85c5-ec8bb0986b6f
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies],TimeHole method, IMSVidStreamBufferV2SourceEvent.TimeHole, IMSVidStreamBufferV2SourceEvent::TimeHole, TimeHole, TimeHole method [Microsoft TV Technologies], TimeHole method [Microsoft TV Technologies],IMSVidStreamBufferV2SourceEvent interface, mstv.imsvidstreambufferv2sourceevent_timehole, segment/IMSVidStreamBufferV2SourceEvent::TimeHole
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
 - IMSVidStreamBufferV2SourceEvent::TimeHole
 - segment/IMSVidStreamBufferV2SourceEvent::TimeHole
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
 - IMSVidStreamBufferV2SourceEvent.TimeHole
---

# IMSVidStreamBufferV2SourceEvent::TimeHole


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Fired when the SBE2 source filter receives a <b>STREAMBUFFER_EC_TIMEHOLE</b> event, which indicates playback has reached a gap in recorded content.

## -parameters

### -param StreamOffsetMS [in]

Time of the start of the gap relative to the content start, in milliseconds.

### -param SizeMS [in]

Duration of the gap, in milliseconds.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambufferv2sourceevent">IMSVidStreamBufferV2SourceEvent</a>



<a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-codes">Stream Buffer Engine Event Codes</a>