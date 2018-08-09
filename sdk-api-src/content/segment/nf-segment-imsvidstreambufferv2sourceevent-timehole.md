---
UID: NF:segment.IMSVidStreamBufferV2SourceEvent.TimeHole
title: IMSVidStreamBufferV2SourceEvent::TimeHole
author: windows-sdk-content
description: Fired when the SBE2 source filter receives a STREAMBUFFER_EC_TIMEHOLE event, which indicates playback has reached a gap in recorded content.
old-location: mstv\imsvidstreambufferv2sourceevent_timehole.htm
old-project: mstv
ms.assetid: 2eceda3b-b3d6-4714-85c5-ec8bb0986b6f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies],TimeHole method, IMSVidStreamBufferV2SourceEvent.TimeHole, IMSVidStreamBufferV2SourceEvent::TimeHole, TimeHole, TimeHole method [Microsoft TV Technologies], TimeHole method [Microsoft TV Technologies],IMSVidStreamBufferV2SourceEvent interface, mstv.imsvidstreambufferv2sourceevent_timehole, segment/IMSVidStreamBufferV2SourceEvent::TimeHole
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
 - IMSVidStreamBufferV2SourceEvent.TimeHole
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMSVidStreamBufferV2SourceEvent::TimeHole


## -description


Fired when the SBE2 source filter receives a <b>STREAMBUFFER_EC_TIMEHOLE</b> event, which indicates playback has reached a gap in recorded content.


## -parameters




### -param StreamOffsetMS [in]

Time of the start of the gap relative to the content start, in milliseconds.
          


### -param SizeMS [in]

Duration of the gap, in milliseconds.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ab463f6e-0718-4420-89bc-28b3c447f3a0">IMSVidStreamBufferV2SourceEvent</a>



<a href="https://msdn.microsoft.com/84364aa4-7306-40ee-9f4d-0683c47965b5">Stream Buffer Engine Event Codes</a>
 

 

