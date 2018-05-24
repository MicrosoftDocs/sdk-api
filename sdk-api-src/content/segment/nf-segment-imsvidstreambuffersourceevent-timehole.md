---
UID: NF:segment.IMSVidStreamBufferSourceEvent.TimeHole
title: IMSVidStreamBufferSourceEvent::TimeHole
author: windows-driver-content
description: This topic applies to Windows XP Service Pack 1 or later.
old-location: mstv\imsvidstreambuffersourceevent_timehole.htm
old-project: mstv
ms.assetid: 6f1c3d20-7ae2-4223-8481-c22ef8422531
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IMSVidStreamBufferSourceEvent interface [Microsoft TV Technologies],TimeHole method, IMSVidStreamBufferSourceEvent.TimeHole, IMSVidStreamBufferSourceEvent::TimeHole, IMSVidStreamBufferSourceEventTimeHole, TimeHole, TimeHole method [Microsoft TV Technologies], TimeHole method [Microsoft TV Technologies],IMSVidStreamBufferSourceEvent interface, mstv.imsvidstreambuffersourceevent_timehole, segment/IMSVidStreamBufferSourceEvent::TimeHole
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
-	IMSVidStreamBufferSourceEvent.TimeHole
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidStreamBufferSourceEvent::TimeHole


## -description



This topic applies to Windows XP Service Pack 1 or later.
        



The <b>TimeHole</b> method is called when playback reaches a gap in the recorded content.


## -parameters




### -param StreamOffsetMS [in]

Specifies the start of the gap, in milliseconds, relative to the content start.


### -param SizeMS [in]

Specifies the length of the gap, in milliseconds.


## -returns



Return S_OK or an error code.




## -remarks



This event corresponds to the STREAMBUFFER_EC_TIMEHOLE event in the Stream Buffer Engine. See <a href="https://msdn.microsoft.com/84364aa4-7306-40ee-9f4d-0683c47965b5">Stream Buffer Engine Event Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/6d8e0cf3-b4c7-4f3e-acff-50f12b8340a8">IMSVidStreamBufferSourceEvent Interface</a>
 

 

