---
UID: NF:segment.IMSVidStreamBufferSourceEvent.StaleDataRead
title: IMSVidStreamBufferSourceEvent::StaleDataRead
author: windows-sdk-content
description: This topic applies to Windows XP Service Pack 1 or later.
old-location: mstv\imsvidstreambuffersourceevent_staledataread.htm
tech.root: MSTV
ms.assetid: ad8da4d8-9c8c-40e6-9fd4-a32cf8e775ce
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IMSVidStreamBufferSourceEvent interface [Microsoft TV Technologies],StaleDataRead method, IMSVidStreamBufferSourceEvent.StaleDataRead, IMSVidStreamBufferSourceEvent::StaleDataRead, IMSVidStreamBufferSourceEventStaleDataRead, StaleDataRead, StaleDataRead method [Microsoft TV Technologies], StaleDataRead method [Microsoft TV Technologies],IMSVidStreamBufferSourceEvent interface, mstv.imsvidstreambuffersourceevent_staledataread, segment/IMSVidStreamBufferSourceEvent::StaleDataRead
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidStreamBufferSourceEvent.StaleDataRead
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidStreamBufferSourceEvent::StaleDataRead


## -description



This topic applies to Windows XP Service Pack 1 or later.
        



The <b>TimeHole</b> method is called when the <b>MSVidStreamBufferSource</b> object reads from a temporary recording file that has been marked for deletion.


## -parameters






## -returns



Return S_OK or an error code.




## -remarks



This event corresponds to the STREAMBUFFER_EC_STALE_DATA_READ event in the Stream Buffer Engine. See <a href="https://msdn.microsoft.com/84364aa4-7306-40ee-9f4d-0683c47965b5">Stream Buffer Engine Event Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/6d8e0cf3-b4c7-4f3e-acff-50f12b8340a8">IMSVidStreamBufferSourceEvent Interface</a>
 

 

