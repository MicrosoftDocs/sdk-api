---
UID: NF:segment.IMSVidStreamBufferSourceEvent.RatingsUnblocked
title: IMSVidStreamBufferSourceEvent::RatingsUnblocked (segment.h)
description: This topic applies to Windows XP Service Pack 1 or later.
helpviewer_keywords: ["IMSVidStreamBufferSourceEvent interface [Microsoft TV Technologies]","RatingsUnblocked method","IMSVidStreamBufferSourceEvent.RatingsUnblocked","IMSVidStreamBufferSourceEvent::RatingsUnblocked","IMSVidStreamBufferSourceEventRatingsUnblocked","RatingsUnblocked","RatingsUnblocked method [Microsoft TV Technologies]","RatingsUnblocked method [Microsoft TV Technologies]","IMSVidStreamBufferSourceEvent interface","mstv.imsvidstreambuffersourceevent_ratingsunblocked","segment/IMSVidStreamBufferSourceEvent::RatingsUnblocked"]
old-location: mstv\imsvidstreambuffersourceevent_ratingsunblocked.htm
tech.root: mstv
ms.assetid: a255df5b-f7fe-4f99-9d29-59e30b922975
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSourceEvent interface [Microsoft TV Technologies],RatingsUnblocked method, IMSVidStreamBufferSourceEvent.RatingsUnblocked, IMSVidStreamBufferSourceEvent::RatingsUnblocked, IMSVidStreamBufferSourceEventRatingsUnblocked, RatingsUnblocked, RatingsUnblocked method [Microsoft TV Technologies], RatingsUnblocked method [Microsoft TV Technologies],IMSVidStreamBufferSourceEvent interface, mstv.imsvidstreambuffersourceevent_ratingsunblocked, segment/IMSVidStreamBufferSourceEvent::RatingsUnblocked
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
 - IMSVidStreamBufferSourceEvent::RatingsUnblocked
 - segment/IMSVidStreamBufferSourceEvent::RatingsUnblocked
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
 - IMSVidStreamBufferSourceEvent.RatingsUnblocked
---

# IMSVidStreamBufferSourceEvent::RatingsUnblocked


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Windows XP Service Pack 1 or later.
        



The <b>RatingsUnblocked</b> method is called when the object unblocks the stream. This event occurs only if a stream that was previously blocked is unblocked.



## -returns

Return S_OK or an error code.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambuffersourceevent">IMSVidStreamBufferSourceEvent Interface</a>
