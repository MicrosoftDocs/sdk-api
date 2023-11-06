---
UID: NF:segment.IMSVidStreamBufferSourceEvent.StaleFileDeleted
title: IMSVidStreamBufferSourceEvent::StaleFileDeleted (segment.h)
description: This topic applies to Windows XP Service Pack 1 or later.
helpviewer_keywords: ["IMSVidStreamBufferSourceEvent interface [Microsoft TV Technologies]","StaleFileDeleted method","IMSVidStreamBufferSourceEvent.StaleFileDeleted","IMSVidStreamBufferSourceEvent::StaleFileDeleted","IMSVidStreamBufferSourceEventStateFileDeleted","StaleFileDeleted","StaleFileDeleted method [Microsoft TV Technologies]","StaleFileDeleted method [Microsoft TV Technologies]","IMSVidStreamBufferSourceEvent interface","mstv.imsvidstreambuffersourceevent_stalefiledeleted","segment/IMSVidStreamBufferSourceEvent::StaleFileDeleted"]
old-location: mstv\imsvidstreambuffersourceevent_stalefiledeleted.htm
tech.root: mstv
ms.assetid: 400efb81-6e16-4065-a9d8-3f0a801f306e
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSourceEvent interface [Microsoft TV Technologies],StaleFileDeleted method, IMSVidStreamBufferSourceEvent.StaleFileDeleted, IMSVidStreamBufferSourceEvent::StaleFileDeleted, IMSVidStreamBufferSourceEventStateFileDeleted, StaleFileDeleted, StaleFileDeleted method [Microsoft TV Technologies], StaleFileDeleted method [Microsoft TV Technologies],IMSVidStreamBufferSourceEvent interface, mstv.imsvidstreambuffersourceevent_stalefiledeleted, segment/IMSVidStreamBufferSourceEvent::StaleFileDeleted
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
 - IMSVidStreamBufferSourceEvent::StaleFileDeleted
 - segment/IMSVidStreamBufferSourceEvent::StaleFileDeleted
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
 - IMSVidStreamBufferSourceEvent.StaleFileDeleted
---

# IMSVidStreamBufferSourceEvent::StaleFileDeleted


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Windows XP Service Pack 1 or later.
        



The <b>StaleFileDeleted</b> method is called when a temporary recording file is deleted.



## -returns

Return S_OK or an error code.

## -remarks

This event corresponds to the STREAMBUFFER_EC_STALE_FILE_DELETED event in the Stream Buffer Engine. See <a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-codes">Stream Buffer Engine Event Codes</a>.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambuffersourceevent">IMSVidStreamBufferSourceEvent Interface</a>
