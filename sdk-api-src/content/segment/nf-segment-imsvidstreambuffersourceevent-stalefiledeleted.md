---
UID: NF:segment.IMSVidStreamBufferSourceEvent.StaleFileDeleted
title: IMSVidStreamBufferSourceEvent::StaleFileDeleted
author: windows-driver-content
description: This topic applies to Windows XP Service Pack 1 or later.
old-location: mstv\imsvidstreambuffersourceevent_stalefiledeleted.htm
old-project: mstv
ms.assetid: 400efb81-6e16-4065-a9d8-3f0a801f306e
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IMSVidStreamBufferSourceEvent interface [Microsoft TV Technologies],StaleFileDeleted method, IMSVidStreamBufferSourceEvent.StaleFileDeleted, IMSVidStreamBufferSourceEvent::StaleFileDeleted, IMSVidStreamBufferSourceEventStateFileDeleted, StaleFileDeleted, StaleFileDeleted method [Microsoft TV Technologies], StaleFileDeleted method [Microsoft TV Technologies],IMSVidStreamBufferSourceEvent interface, mstv.imsvidstreambuffersourceevent_stalefiledeleted, segment/IMSVidStreamBufferSourceEvent::StaleFileDeleted
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
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidStreamBufferSourceEvent.StaleFileDeleted
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidStreamBufferSourceEvent::StaleFileDeleted


## -description



This topic applies to Windows XP Service Pack 1 or later.
        



The <b>StaleFileDeleted</b> method is called when a temporary recording file is deleted.


## -parameters






## -returns



Return S_OK or an error code.




## -remarks



This event corresponds to the STREAMBUFFER_EC_STALE_FILE_DELETED event in the Stream Buffer Engine. See <a href="https://msdn.microsoft.com/84364aa4-7306-40ee-9f4d-0683c47965b5">Stream Buffer Engine Event Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/6d8e0cf3-b4c7-4f3e-acff-50f12b8340a8">IMSVidStreamBufferSourceEvent Interface</a>
 

 

