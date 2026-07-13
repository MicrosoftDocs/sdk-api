---
UID: NF:segment.IMSVidStreamBufferSourceEvent.RatingsBlocked
title: IMSVidStreamBufferSourceEvent::RatingsBlocked (segment.h)
description: This topic applies to Windows XP Service Pack 1 or later.
helpviewer_keywords: ["IMSVidStreamBufferSourceEvent interface [Microsoft TV Technologies]","RatingsBlocked method","IMSVidStreamBufferSourceEvent.RatingsBlocked","IMSVidStreamBufferSourceEvent::RatingsBlocked","IMSVidStreamBufferSourceEventRatingsBlocked","RatingsBlocked","RatingsBlocked method [Microsoft TV Technologies]","RatingsBlocked method [Microsoft TV Technologies]","IMSVidStreamBufferSourceEvent interface","mstv.imsvidstreambuffersourceevent_ratingsblocked","segment/IMSVidStreamBufferSourceEvent::RatingsBlocked"]
old-location: mstv\imsvidstreambuffersourceevent_ratingsblocked.htm
tech.root: mstv
ms.assetid: 1d5e510e-9629-4249-a704-b7a995d27edf
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSourceEvent interface [Microsoft TV Technologies],RatingsBlocked method, IMSVidStreamBufferSourceEvent.RatingsBlocked, IMSVidStreamBufferSourceEvent::RatingsBlocked, IMSVidStreamBufferSourceEventRatingsBlocked, RatingsBlocked, RatingsBlocked method [Microsoft TV Technologies], RatingsBlocked method [Microsoft TV Technologies],IMSVidStreamBufferSourceEvent interface, mstv.imsvidstreambuffersourceevent_ratingsblocked, segment/IMSVidStreamBufferSourceEvent::RatingsBlocked
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
 - IMSVidStreamBufferSourceEvent::RatingsBlocked
 - segment/IMSVidStreamBufferSourceEvent::RatingsBlocked
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
 - IMSVidStreamBufferSourceEvent.RatingsBlocked
---

# IMSVidStreamBufferSourceEvent::RatingsBlocked


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Windows XP Service Pack 1 or later.
        



The <b>RatingsBlocked</b> method is called when the object blocks the stream, which occurs if the rating is not allowed under the current permissions.



## -returns

Return S_OK or an error code.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambuffersourceevent">IMSVidStreamBufferSourceEvent Interface</a>
