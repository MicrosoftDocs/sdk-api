---
UID: NF:segment.IMSVidStreamBufferV2SourceEvent.BroadcastEvent
title: IMSVidStreamBufferV2SourceEvent::BroadcastEvent
author: windows-sdk-content
description: Fired when the SBE2 source filter receives any event fired through the IBroadcastEvent interface, other than the EVENTID_DTFilterRatingChange event.
old-location: mstv\imsvidstreambufferv2sourceevent_broadcastevent.htm
old-project: mstv
ms.assetid: f5d5b6d8-9baa-4a9e-8275-e817394c211a
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: BroadcastEvent, BroadcastEvent method [Microsoft TV Technologies], BroadcastEvent method [Microsoft TV Technologies],IMSVidStreamBufferV2SourceEvent interface, IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies],BroadcastEvent method, IMSVidStreamBufferV2SourceEvent.BroadcastEvent, IMSVidStreamBufferV2SourceEvent::BroadcastEvent, mstv.imsvidstreambufferv2sourceevent_broadcastevent, segment/IMSVidStreamBufferV2SourceEvent::BroadcastEvent
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SourceSizeList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidStreamBufferV2SourceEvent.BroadcastEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidStreamBufferV2SourceEvent::BroadcastEvent


## -description



      Fired when the SBE2 source filter receives any event fired through the <a href="https://msdn.microsoft.com/90d4fbc7-d552-460b-96b2-77e2347af716">IBroadcastEvent</a> interface, other than  the <b>EVENTID_DTFilterRatingChange</b> event.


## -parameters




### -param Guid [in]

<b>BSTR</b> object that contains the GUID that identifies the event.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/90d4fbc7-d552-460b-96b2-77e2347af716">IBroadcastEvent</a>



<a href="https://msdn.microsoft.com/ab463f6e-0718-4420-89bc-28b3c447f3a0">IMSVidStreamBufferV2SourceEvent</a>
 

 

