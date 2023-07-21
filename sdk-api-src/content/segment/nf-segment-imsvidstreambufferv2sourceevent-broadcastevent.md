---
UID: NF:segment.IMSVidStreamBufferV2SourceEvent.BroadcastEvent
title: IMSVidStreamBufferV2SourceEvent::BroadcastEvent (segment.h)
description: Fired when the SBE2 source filter receives any event fired through the IBroadcastEvent interface, other than the EVENTID_DTFilterRatingChange event.
helpviewer_keywords: ["BroadcastEvent","BroadcastEvent method [Microsoft TV Technologies]","BroadcastEvent method [Microsoft TV Technologies]","IMSVidStreamBufferV2SourceEvent interface","IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies]","BroadcastEvent method","IMSVidStreamBufferV2SourceEvent.BroadcastEvent","IMSVidStreamBufferV2SourceEvent::BroadcastEvent","mstv.imsvidstreambufferv2sourceevent_broadcastevent","segment/IMSVidStreamBufferV2SourceEvent::BroadcastEvent"]
old-location: mstv\imsvidstreambufferv2sourceevent_broadcastevent.htm
tech.root: mstv
ms.assetid: f5d5b6d8-9baa-4a9e-8275-e817394c211a
ms.date: 12/05/2018
ms.keywords: BroadcastEvent, BroadcastEvent method [Microsoft TV Technologies], BroadcastEvent method [Microsoft TV Technologies],IMSVidStreamBufferV2SourceEvent interface, IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies],BroadcastEvent method, IMSVidStreamBufferV2SourceEvent.BroadcastEvent, IMSVidStreamBufferV2SourceEvent::BroadcastEvent, mstv.imsvidstreambufferv2sourceevent_broadcastevent, segment/IMSVidStreamBufferV2SourceEvent::BroadcastEvent
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
 - IMSVidStreamBufferV2SourceEvent::BroadcastEvent
 - segment/IMSVidStreamBufferV2SourceEvent::BroadcastEvent
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
 - IMSVidStreamBufferV2SourceEvent.BroadcastEvent
---

# IMSVidStreamBufferV2SourceEvent::BroadcastEvent


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Fired when the SBE2 source filter receives any event fired through the <a href="/previous-versions/dd376294(v=vs.85)">IBroadcastEvent</a> interface, other than  the <b>EVENTID_DTFilterRatingChange</b> event.

## -parameters

### -param Guid [in]

<b>BSTR</b> object that contains the GUID that identifies the event.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/dd376294(v=vs.85)">IBroadcastEvent</a>



<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambufferv2sourceevent">IMSVidStreamBufferV2SourceEvent</a>