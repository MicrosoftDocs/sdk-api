---
UID: NF:segment.IMSVidStreamBufferV2SourceEvent.StaleFileDeleted
title: IMSVidStreamBufferV2SourceEvent::StaleFileDeleted (segment.h)
description: Fired when the SBE2 source filter receives a STREAMBUFFER_EC_STALE_FILE_DELETED event, which indicates that a temporary file has been deleted.
helpviewer_keywords: ["IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies]","StaleFileDeleted method","IMSVidStreamBufferV2SourceEvent.StaleFileDeleted","IMSVidStreamBufferV2SourceEvent::StaleFileDeleted","StaleFileDeleted","StaleFileDeleted method [Microsoft TV Technologies]","StaleFileDeleted method [Microsoft TV Technologies]","IMSVidStreamBufferV2SourceEvent interface","mstv.imsvidstreambufferv2sourceevent_stalefiledeleted","segment/IMSVidStreamBufferV2SourceEvent::StaleFileDeleted"]
old-location: mstv\imsvidstreambufferv2sourceevent_stalefiledeleted.htm
tech.root: mstv
ms.assetid: 23cd93d9-3615-4fbf-a6de-61ee69cd51e3
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies],StaleFileDeleted method, IMSVidStreamBufferV2SourceEvent.StaleFileDeleted, IMSVidStreamBufferV2SourceEvent::StaleFileDeleted, StaleFileDeleted, StaleFileDeleted method [Microsoft TV Technologies], StaleFileDeleted method [Microsoft TV Technologies],IMSVidStreamBufferV2SourceEvent interface, mstv.imsvidstreambufferv2sourceevent_stalefiledeleted, segment/IMSVidStreamBufferV2SourceEvent::StaleFileDeleted
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
 - IMSVidStreamBufferV2SourceEvent::StaleFileDeleted
 - segment/IMSVidStreamBufferV2SourceEvent::StaleFileDeleted
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
 - IMSVidStreamBufferV2SourceEvent.StaleFileDeleted
---

# IMSVidStreamBufferV2SourceEvent::StaleFileDeleted


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Fired when the SBE2 source filter receives a <b>STREAMBUFFER_EC_STALE_FILE_DELETED</b> event, which indicates that a temporary file has been deleted.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambufferv2sourceevent">IMSVidStreamBufferV2SourceEvent</a>



<a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-codes">Stream Buffer Engine Event Codes</a>
