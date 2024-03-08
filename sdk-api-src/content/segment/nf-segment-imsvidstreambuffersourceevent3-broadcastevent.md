---
UID: NF:segment.IMSVidStreamBufferSourceEvent3.BroadcastEvent
title: IMSVidStreamBufferSourceEvent3::BroadcastEvent (segment.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["BroadcastEvent","BroadcastEvent method [Microsoft TV Technologies]","BroadcastEvent method [Microsoft TV Technologies]","IMSVidStreamBufferSourceEvent3 interface","IMSVidStreamBufferSourceEvent3 interface [Microsoft TV Technologies]","BroadcastEvent method","IMSVidStreamBufferSourceEvent3.BroadcastEvent","IMSVidStreamBufferSourceEvent3::BroadcastEvent","IMSVidStreamBufferSourceEvent3BroadcastEvent","mstv.imsvidstreambuffersourceevent3_broadcastevent","segment/IMSVidStreamBufferSourceEvent3::BroadcastEvent"]
old-location: mstv\imsvidstreambuffersourceevent3_broadcastevent.htm
tech.root: mstv
ms.assetid: 05eeb539-3a0a-4a00-abe5-0a014629d186
ms.date: 12/05/2018
ms.keywords: BroadcastEvent, BroadcastEvent method [Microsoft TV Technologies], BroadcastEvent method [Microsoft TV Technologies],IMSVidStreamBufferSourceEvent3 interface, IMSVidStreamBufferSourceEvent3 interface [Microsoft TV Technologies],BroadcastEvent method, IMSVidStreamBufferSourceEvent3.BroadcastEvent, IMSVidStreamBufferSourceEvent3::BroadcastEvent, IMSVidStreamBufferSourceEvent3BroadcastEvent, mstv.imsvidstreambuffersourceevent3_broadcastevent, segment/IMSVidStreamBufferSourceEvent3::BroadcastEvent
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
 - IMSVidStreamBufferSourceEvent3::BroadcastEvent
 - segment/IMSVidStreamBufferSourceEvent3::BroadcastEvent
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
 - IMSVidStreamBufferSourceEvent3.BroadcastEvent
---

# IMSVidStreamBufferSourceEvent3::BroadcastEvent


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>BroadcastEvent</b> method is called when the <a href="/previous-versions/windows/desktop/legacy/dd695136(v=vs.85)">MSVidStreamBufferSource</a> object receives a broadcast event through the <a href="/previous-versions/dd376294(v=vs.85)">IBroadcastEvent</a> interface.

## -parameters

### -param Guid [in]

GUID that specifies the event. For more information, see <a href="/previous-versions/ms784798(v=vs.85)">IBroadcastEvent::Fire</a>.

## -returns

Return S_OK or an error code.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambuffersourceevent3">IMSVidStreamBufferSourceEvent3 Interface</a>