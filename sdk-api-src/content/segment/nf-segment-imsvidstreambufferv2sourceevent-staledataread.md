---
UID: NF:segment.IMSVidStreamBufferV2SourceEvent.StaleDataRead
title: IMSVidStreamBufferV2SourceEvent::StaleDataRead (segment.h)
author: windows-sdk-content
description: Fired when the SBE2 source filter receives a STREAMBUFFER_EC_STALE_DATA_READ event, which indicates an MSVidStreamBufferSource object has read from a temporary recording file that is marked for deletion.
old-location: mstv\imsvidstreambufferv2sourceevent_staledataread.htm
tech.root: mstv
ms.assetid: 8eb53b77-94a3-4216-a32f-22338d84f5ad
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies],StaleDataRead method, IMSVidStreamBufferV2SourceEvent.StaleDataRead, IMSVidStreamBufferV2SourceEvent::StaleDataRead, StaleDataRead, StaleDataRead method [Microsoft TV Technologies], StaleDataRead method [Microsoft TV Technologies],IMSVidStreamBufferV2SourceEvent interface, mstv.imsvidstreambufferv2sourceevent_staledataread, segment/IMSVidStreamBufferV2SourceEvent::StaleDataRead
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidStreamBufferV2SourceEvent.StaleDataRead
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidStreamBufferV2SourceEvent::StaleDataRead


## -description


Fired when the SBE2 source filter receives a <b>STREAMBUFFER_EC_STALE_DATA_READ</b> event, which indicates an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd695136(v=vs.85)">MSVidStreamBufferSource</a> object has read from a temporary recording file that is marked for deletion.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidstreambufferv2sourceevent">IMSVidStreamBufferV2SourceEvent</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/stream-buffer-engine-codes">Stream Buffer Engine Event Codes</a>
 

 

