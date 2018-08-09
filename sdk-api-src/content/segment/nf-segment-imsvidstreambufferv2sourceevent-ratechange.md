---
UID: NF:segment.IMSVidStreamBufferV2SourceEvent.RateChange
title: IMSVidStreamBufferV2SourceEvent::RateChange
author: windows-sdk-content
description: Fired when the SBE2 source filter receives a STREAMBUFFER_EC_RATE_CHANGED event, which indicates the playback rate has changed.
old-location: mstv\imsvidstreambufferv2sourceevent_ratechange.htm
old-project: mstv
ms.assetid: 32af2323-0018-4e77-bf2e-9ff95e59f91e
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies],RateChange method, IMSVidStreamBufferV2SourceEvent.RateChange, IMSVidStreamBufferV2SourceEvent::RateChange, RateChange, RateChange method [Microsoft TV Technologies], RateChange method [Microsoft TV Technologies],IMSVidStreamBufferV2SourceEvent interface, mstv.imsvidstreambufferv2sourceevent_ratechange, segment/IMSVidStreamBufferV2SourceEvent::RateChange
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
 - IMSVidStreamBufferV2SourceEvent.RateChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMSVidStreamBufferV2SourceEvent::RateChange


## -description


Fired when the SBE2 source filter receives a <b>STREAMBUFFER_EC_RATE_CHANGED</b> event, which indicates the playback rate has changed.


## -parameters




### -param qwNewRate [in]

New playback rate, multiplied by 1,000. 
          


### -param qwOldRate [in]

Old playback rate, multiplied by 1,000.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ab463f6e-0718-4420-89bc-28b3c447f3a0">IMSVidStreamBufferV2SourceEvent</a>



<a href="https://msdn.microsoft.com/84364aa4-7306-40ee-9f4d-0683c47965b5">Stream Buffer Engine Event Codes</a>
 

 

