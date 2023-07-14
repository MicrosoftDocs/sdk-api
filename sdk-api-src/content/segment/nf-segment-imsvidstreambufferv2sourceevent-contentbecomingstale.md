---
UID: NF:segment.IMSVidStreamBufferV2SourceEvent.ContentBecomingStale
title: IMSVidStreamBufferV2SourceEvent::ContentBecomingStale (segment.h)
description: Fired when the SBE2 source filter receives a STREAMBUFFER_EC_CONTENT_BECOMING_STALE event, which indicates the stream buffer source lags behind the stream buffer sink by more than a preset number of files.For more information, see IStreamBufferConfigure::GetBackingFileCount.
helpviewer_keywords: ["ContentBecomingStale","ContentBecomingStale method [Microsoft TV Technologies]","ContentBecomingStale method [Microsoft TV Technologies]","IMSVidStreamBufferV2SourceEvent interface","IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies]","ContentBecomingStale method","IMSVidStreamBufferV2SourceEvent.ContentBecomingStale","IMSVidStreamBufferV2SourceEvent::ContentBecomingStale","mstv.imsvidstreambufferv2sourceevent_contentbecomingstale","segment/IMSVidStreamBufferV2SourceEvent::ContentBecomingStale"]
old-location: mstv\imsvidstreambufferv2sourceevent_contentbecomingstale.htm
tech.root: mstv
ms.assetid: b9af548a-9796-4dc0-8b78-46e529a484ce
ms.date: 12/05/2018
ms.keywords: ContentBecomingStale, ContentBecomingStale method [Microsoft TV Technologies], ContentBecomingStale method [Microsoft TV Technologies],IMSVidStreamBufferV2SourceEvent interface, IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies],ContentBecomingStale method, IMSVidStreamBufferV2SourceEvent.ContentBecomingStale, IMSVidStreamBufferV2SourceEvent::ContentBecomingStale, mstv.imsvidstreambufferv2sourceevent_contentbecomingstale, segment/IMSVidStreamBufferV2SourceEvent::ContentBecomingStale
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
 - IMSVidStreamBufferV2SourceEvent::ContentBecomingStale
 - segment/IMSVidStreamBufferV2SourceEvent::ContentBecomingStale
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
 - IMSVidStreamBufferV2SourceEvent.ContentBecomingStale
---

# IMSVidStreamBufferV2SourceEvent::ContentBecomingStale


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Fired when the SBE2 source filter receives a <b>STREAMBUFFER_EC_CONTENT_BECOMING_STALE</b> event, which indicates  the stream buffer source lags behind the stream buffer sink by more than a preset number of files.

For more information, see <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferconfigure-getbackingfilecount">IStreamBufferConfigure::GetBackingFileCount</a>.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambufferv2sourceevent">IMSVidStreamBufferV2SourceEvent</a>



<a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferconfigure-getbackingfilecount">IStreamBufferConfigure::GetBackingFileCount</a>



<a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-codes">Stream Buffer Engine Event Codes</a>
