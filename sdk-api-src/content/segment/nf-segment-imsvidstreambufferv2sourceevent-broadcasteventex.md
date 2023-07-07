---
UID: NF:segment.IMSVidStreamBufferV2SourceEvent.BroadcastEventEx
title: IMSVidStreamBufferV2SourceEvent::BroadcastEventEx (segment.h)
description: Fired when an SBE2 source filter receives any event fired by a call to IBroadcastEventEx::FireEx.
helpviewer_keywords: ["BroadcastEventEx","BroadcastEventEx method [Microsoft TV Technologies]","BroadcastEventEx method [Microsoft TV Technologies]","IMSVidStreamBufferV2SourceEvent interface","IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies]","BroadcastEventEx method","IMSVidStreamBufferV2SourceEvent.BroadcastEventEx","IMSVidStreamBufferV2SourceEvent::BroadcastEventEx","mstv.imsvidstreambufferv2sourceevent_broadcasteventex","segment/IMSVidStreamBufferV2SourceEvent::BroadcastEventEx"]
old-location: mstv\imsvidstreambufferv2sourceevent_broadcasteventex.htm
tech.root: mstv
ms.assetid: 731baecc-72f9-4ecd-bc01-40ad31c67051
ms.date: 12/05/2018
ms.keywords: BroadcastEventEx, BroadcastEventEx method [Microsoft TV Technologies], BroadcastEventEx method [Microsoft TV Technologies],IMSVidStreamBufferV2SourceEvent interface, IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies],BroadcastEventEx method, IMSVidStreamBufferV2SourceEvent.BroadcastEventEx, IMSVidStreamBufferV2SourceEvent::BroadcastEventEx, mstv.imsvidstreambufferv2sourceevent_broadcasteventex, segment/IMSVidStreamBufferV2SourceEvent::BroadcastEventEx
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
 - IMSVidStreamBufferV2SourceEvent::BroadcastEventEx
 - segment/IMSVidStreamBufferV2SourceEvent::BroadcastEventEx
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
 - IMSVidStreamBufferV2SourceEvent.BroadcastEventEx
---

# IMSVidStreamBufferV2SourceEvent::BroadcastEventEx


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Fired when an SBE2 source filter receives any event fired by a call to <a href="/previous-versions/dd376296(v=vs.85)">IBroadcastEventEx::FireEx</a>.

## -parameters

### -param Guid [in]

<b>BSTR</b> object that contains the GUID that identifies the event.

### -param Param1 [in]

Specifies the first implementation-dependent parameter.

### -param Param2 [in]

Specifies the second implementation-dependent parameter.

### -param Param3 [in]

Specifies the third implementation-dependent parameter.

### -param Param4 [in]

Specifies the fourth implementation-dependent parameter.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/dd376296(v=vs.85)">IBroadcastEventEx::FireEx</a>



<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambufferv2sourceevent">IMSVidStreamBufferV2SourceEvent</a>