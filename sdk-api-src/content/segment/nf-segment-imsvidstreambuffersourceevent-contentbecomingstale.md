---
UID: NF:segment.IMSVidStreamBufferSourceEvent.ContentBecomingStale
title: IMSVidStreamBufferSourceEvent::ContentBecomingStale
author: windows-driver-content
description: This topic applies to Windows XP Service Pack 1 or later.
old-location: mstv\imsvidstreambuffersourceevent_contentbecomingstale.htm
old-project: mstv
ms.assetid: ff28174c-a5a7-4cd3-b967-3e52d53864f3
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: ContentBecomingStale, ContentBecomingStale method [Microsoft TV Technologies], ContentBecomingStale method [Microsoft TV Technologies],IMSVidStreamBufferSourceEvent interface, IMSVidStreamBufferSourceEvent interface [Microsoft TV Technologies],ContentBecomingStale method, IMSVidStreamBufferSourceEvent.ContentBecomingStale, IMSVidStreamBufferSourceEvent::ContentBecomingStale, IMSVidStreamBufferSourceEventContentBecomingStale, mstv.imsvidstreambuffersourceevent_contentbecomingstale, segment/IMSVidStreamBufferSourceEvent::ContentBecomingStale
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
-	IMSVidStreamBufferSourceEvent.ContentBecomingStale
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidStreamBufferSourceEvent::ContentBecomingStale


## -description



This topic applies to Windows XP Service Pack 1 or later.
        



The <b>CertificateSuccess</b> method is called when the stream buffer source lags behind the stream buffer sink by more than a preset number of files.


## -parameters






## -returns



Return S_OK or an error code.




## -remarks



This event corresponds to the STREAMBUFFER_EC_CONTENT_BECOMING_STALE event in the Stream Buffer Engine. See <a href="https://msdn.microsoft.com/84364aa4-7306-40ee-9f4d-0683c47965b5">Stream Buffer Engine Event Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/6d8e0cf3-b4c7-4f3e-acff-50f12b8340a8">IMSVidStreamBufferSourceEvent Interface</a>
 

 

