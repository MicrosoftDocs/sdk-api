---
UID: NF:segment.IMSVidStreamBufferSourceEvent.StaleDataRead
title: IMSVidStreamBufferSourceEvent::StaleDataRead (segment.h)
description: This topic applies to Windows XP Service Pack 1 or later.
helpviewer_keywords: ["IMSVidStreamBufferSourceEvent interface [Microsoft TV Technologies]","StaleDataRead method","IMSVidStreamBufferSourceEvent.StaleDataRead","IMSVidStreamBufferSourceEvent::StaleDataRead","IMSVidStreamBufferSourceEventStaleDataRead","StaleDataRead","StaleDataRead method [Microsoft TV Technologies]","StaleDataRead method [Microsoft TV Technologies]","IMSVidStreamBufferSourceEvent interface","mstv.imsvidstreambuffersourceevent_staledataread","segment/IMSVidStreamBufferSourceEvent::StaleDataRead"]
old-location: mstv\imsvidstreambuffersourceevent_staledataread.htm
tech.root: mstv
ms.assetid: ad8da4d8-9c8c-40e6-9fd4-a32cf8e775ce
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSourceEvent interface [Microsoft TV Technologies],StaleDataRead method, IMSVidStreamBufferSourceEvent.StaleDataRead, IMSVidStreamBufferSourceEvent::StaleDataRead, IMSVidStreamBufferSourceEventStaleDataRead, StaleDataRead, StaleDataRead method [Microsoft TV Technologies], StaleDataRead method [Microsoft TV Technologies],IMSVidStreamBufferSourceEvent interface, mstv.imsvidstreambuffersourceevent_staledataread, segment/IMSVidStreamBufferSourceEvent::StaleDataRead
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
 - IMSVidStreamBufferSourceEvent::StaleDataRead
 - segment/IMSVidStreamBufferSourceEvent::StaleDataRead
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
 - IMSVidStreamBufferSourceEvent.StaleDataRead
---

# IMSVidStreamBufferSourceEvent::StaleDataRead


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Windows XP Service Pack 1 or later.
        



The <b>TimeHole</b> method is called when the <b>MSVidStreamBufferSource</b> object reads from a temporary recording file that has been marked for deletion.



## -returns

Return S_OK or an error code.

## -remarks

This event corresponds to the STREAMBUFFER_EC_STALE_DATA_READ event in the Stream Buffer Engine. See <a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-codes">Stream Buffer Engine Event Codes</a>.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambuffersourceevent">IMSVidStreamBufferSourceEvent Interface</a>
