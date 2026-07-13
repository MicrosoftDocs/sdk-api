---
UID: NF:segment.IMSVidStreamBufferSourceEvent.ContentBecomingStale
title: IMSVidStreamBufferSourceEvent::ContentBecomingStale (segment.h)
description: This topic applies to Windows XP Service Pack 1 or later.
helpviewer_keywords: ["ContentBecomingStale","ContentBecomingStale method [Microsoft TV Technologies]","ContentBecomingStale method [Microsoft TV Technologies]","IMSVidStreamBufferSourceEvent interface","IMSVidStreamBufferSourceEvent interface [Microsoft TV Technologies]","ContentBecomingStale method","IMSVidStreamBufferSourceEvent.ContentBecomingStale","IMSVidStreamBufferSourceEvent::ContentBecomingStale","IMSVidStreamBufferSourceEventContentBecomingStale","mstv.imsvidstreambuffersourceevent_contentbecomingstale","segment/IMSVidStreamBufferSourceEvent::ContentBecomingStale"]
old-location: mstv\imsvidstreambuffersourceevent_contentbecomingstale.htm
tech.root: mstv
ms.assetid: ff28174c-a5a7-4cd3-b967-3e52d53864f3
ms.date: 12/05/2018
ms.keywords: ContentBecomingStale, ContentBecomingStale method [Microsoft TV Technologies], ContentBecomingStale method [Microsoft TV Technologies],IMSVidStreamBufferSourceEvent interface, IMSVidStreamBufferSourceEvent interface [Microsoft TV Technologies],ContentBecomingStale method, IMSVidStreamBufferSourceEvent.ContentBecomingStale, IMSVidStreamBufferSourceEvent::ContentBecomingStale, IMSVidStreamBufferSourceEventContentBecomingStale, mstv.imsvidstreambuffersourceevent_contentbecomingstale, segment/IMSVidStreamBufferSourceEvent::ContentBecomingStale
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
 - IMSVidStreamBufferSourceEvent::ContentBecomingStale
 - segment/IMSVidStreamBufferSourceEvent::ContentBecomingStale
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
 - IMSVidStreamBufferSourceEvent.ContentBecomingStale
---

# IMSVidStreamBufferSourceEvent::ContentBecomingStale


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Windows XP Service Pack 1 or later.
        



The <b>CertificateSuccess</b> method is called when the stream buffer source lags behind the stream buffer sink by more than a preset number of files.



## -returns

Return S_OK or an error code.

## -remarks

This event corresponds to the STREAMBUFFER_EC_CONTENT_BECOMING_STALE event in the Stream Buffer Engine. See <a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-codes">Stream Buffer Engine Event Codes</a>.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambuffersourceevent">IMSVidStreamBufferSourceEvent Interface</a>
