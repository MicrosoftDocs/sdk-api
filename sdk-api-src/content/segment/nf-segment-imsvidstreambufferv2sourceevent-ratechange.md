---
UID: NF:segment.IMSVidStreamBufferV2SourceEvent.RateChange
title: IMSVidStreamBufferV2SourceEvent::RateChange (segment.h)
description: Fired when the SBE2 source filter receives a STREAMBUFFER_EC_RATE_CHANGED event, which indicates the playback rate has changed.
helpviewer_keywords: ["IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies]","RateChange method","IMSVidStreamBufferV2SourceEvent.RateChange","IMSVidStreamBufferV2SourceEvent::RateChange","RateChange","RateChange method [Microsoft TV Technologies]","RateChange method [Microsoft TV Technologies]","IMSVidStreamBufferV2SourceEvent interface","mstv.imsvidstreambufferv2sourceevent_ratechange","segment/IMSVidStreamBufferV2SourceEvent::RateChange"]
old-location: mstv\imsvidstreambufferv2sourceevent_ratechange.htm
tech.root: mstv
ms.assetid: 32af2323-0018-4e77-bf2e-9ff95e59f91e
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies],RateChange method, IMSVidStreamBufferV2SourceEvent.RateChange, IMSVidStreamBufferV2SourceEvent::RateChange, RateChange, RateChange method [Microsoft TV Technologies], RateChange method [Microsoft TV Technologies],IMSVidStreamBufferV2SourceEvent interface, mstv.imsvidstreambufferv2sourceevent_ratechange, segment/IMSVidStreamBufferV2SourceEvent::RateChange
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
 - IMSVidStreamBufferV2SourceEvent::RateChange
 - segment/IMSVidStreamBufferV2SourceEvent::RateChange
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
 - IMSVidStreamBufferV2SourceEvent.RateChange
---

# IMSVidStreamBufferV2SourceEvent::RateChange


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Fired when the SBE2 source filter receives a <b>STREAMBUFFER_EC_RATE_CHANGED</b> event, which indicates the playback rate has changed.

## -parameters

### -param qwNewRate [in]

New playback rate, multiplied by 1,000.

### -param qwOldRate [in]

Old playback rate, multiplied by 1,000.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambufferv2sourceevent">IMSVidStreamBufferV2SourceEvent</a>



<a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-codes">Stream Buffer Engine Event Codes</a>