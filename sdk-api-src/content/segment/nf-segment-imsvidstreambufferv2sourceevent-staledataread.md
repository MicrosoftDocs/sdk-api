---
UID: NF:segment.IMSVidStreamBufferV2SourceEvent.StaleDataRead
title: IMSVidStreamBufferV2SourceEvent::StaleDataRead (segment.h)
description: Fired when the SBE2 source filter receives a STREAMBUFFER_EC_STALE_DATA_READ event, which indicates an MSVidStreamBufferSource object has read from a temporary recording file that is marked for deletion.
helpviewer_keywords: ["IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies]","StaleDataRead method","IMSVidStreamBufferV2SourceEvent.StaleDataRead","IMSVidStreamBufferV2SourceEvent::StaleDataRead","StaleDataRead","StaleDataRead method [Microsoft TV Technologies]","StaleDataRead method [Microsoft TV Technologies]","IMSVidStreamBufferV2SourceEvent interface","mstv.imsvidstreambufferv2sourceevent_staledataread","segment/IMSVidStreamBufferV2SourceEvent::StaleDataRead"]
old-location: mstv\imsvidstreambufferv2sourceevent_staledataread.htm
tech.root: mstv
ms.assetid: 8eb53b77-94a3-4216-a32f-22338d84f5ad
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies],StaleDataRead method, IMSVidStreamBufferV2SourceEvent.StaleDataRead, IMSVidStreamBufferV2SourceEvent::StaleDataRead, StaleDataRead, StaleDataRead method [Microsoft TV Technologies], StaleDataRead method [Microsoft TV Technologies],IMSVidStreamBufferV2SourceEvent interface, mstv.imsvidstreambufferv2sourceevent_staledataread, segment/IMSVidStreamBufferV2SourceEvent::StaleDataRead
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
 - IMSVidStreamBufferV2SourceEvent::StaleDataRead
 - segment/IMSVidStreamBufferV2SourceEvent::StaleDataRead
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
 - IMSVidStreamBufferV2SourceEvent.StaleDataRead
---

# IMSVidStreamBufferV2SourceEvent::StaleDataRead


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Fired when the SBE2 source filter receives a <b>STREAMBUFFER_EC_STALE_DATA_READ</b> event, which indicates an <a href="/previous-versions/windows/desktop/legacy/dd695136(v=vs.85)">MSVidStreamBufferSource</a> object has read from a temporary recording file that is marked for deletion.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambufferv2sourceevent">IMSVidStreamBufferV2SourceEvent</a>



<a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-codes">Stream Buffer Engine Event Codes</a>
