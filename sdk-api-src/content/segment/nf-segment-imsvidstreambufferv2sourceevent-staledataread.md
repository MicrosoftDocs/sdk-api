---
UID: NF:segment.IMSVidStreamBufferV2SourceEvent.StaleDataRead
title: IMSVidStreamBufferV2SourceEvent::StaleDataRead method
author: windows-driver-content
description: Fired when the SBE2 source filter receives a STREAMBUFFER_EC_STALE_DATA_READ event, which indicates an MSVidStreamBufferSource object has read from a temporary recording file that is marked for deletion.
old-location: mstv\imsvidstreambufferv2sourceevent_staledataread.htm
old-project: mstv
ms.assetid: 8eb53b77-94a3-4216-a32f-22338d84f5ad
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IMSVidStreamBufferV2SourceEvent, IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies], StaleDataRead method, IMSVidStreamBufferV2SourceEvent::StaleDataRead, StaleDataRead method [Microsoft TV Technologies], StaleDataRead method [Microsoft TV Technologies], IMSVidStreamBufferV2SourceEvent interface, StaleDataRead,IMSVidStreamBufferV2SourceEvent.StaleDataRead, mstv.imsvidstreambufferv2sourceevent_staledataread, segment/IMSVidStreamBufferV2SourceEvent::StaleDataRead
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidStreamBufferV2SourceEvent.StaleDataRead
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMSVidStreamBufferV2SourceEvent::StaleDataRead method


## -description



      Fired when the SBE2 source filter receives a <b>STREAMBUFFER_EC_STALE_DATA_READ</b> event, which indicates an <a href="https://msdn.microsoft.com/4043e199-d329-45f3-80a7-cd84fad88979">MSVidStreamBufferSource</a> object has read from a temporary recording file that is marked for deletion.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ab463f6e-0718-4420-89bc-28b3c447f3a0">IMSVidStreamBufferV2SourceEvent</a>



<a href="https://msdn.microsoft.com/84364aa4-7306-40ee-9f4d-0683c47965b5">Stream Buffer Engine Event Codes</a>
 

 

