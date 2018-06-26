---
UID: NF:segment.IMSVidStreamBufferV2SourceEvent.BroadcastEventEx
title: IMSVidStreamBufferV2SourceEvent::BroadcastEventEx
author: windows-sdk-content
description: Fired when an SBE2 source filter receives any event fired by a call to IBroadcastEventEx::FireEx.
old-location: mstv\imsvidstreambufferv2sourceevent_broadcasteventex.htm
old-project: mstv
ms.assetid: 731baecc-72f9-4ecd-bc01-40ad31c67051
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: BroadcastEventEx, BroadcastEventEx method [Microsoft TV Technologies], BroadcastEventEx method [Microsoft TV Technologies],IMSVidStreamBufferV2SourceEvent interface, IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies],BroadcastEventEx method, IMSVidStreamBufferV2SourceEvent.BroadcastEventEx, IMSVidStreamBufferV2SourceEvent::BroadcastEventEx, mstv.imsvidstreambufferv2sourceevent_broadcasteventex, segment/IMSVidStreamBufferV2SourceEvent::BroadcastEventEx
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
 - IMSVidStreamBufferV2SourceEvent.BroadcastEventEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMSVidStreamBufferV2SourceEvent::BroadcastEventEx


## -description



      
            Fired when an SBE2 source filter receives any event fired by a call to <a href="https://msdn.microsoft.com/b9ad8d9d-9827-44f9-9d2b-3f662c32eb9b">IBroadcastEventEx::FireEx</a>.
          


## -parameters




### -param Guid [in]

<b>BSTR</b> object that contains the GUID that identifies the event.
          


### -param Param1 [in]


            Specifies the first implementation-dependent parameter.
          


### -param Param2 [in]


            Specifies the second implementation-dependent parameter.
          


### -param Param3 [in]


            Specifies the third implementation-dependent parameter.
          


### -param Param4 [in]


            Specifies the fourth implementation-dependent parameter.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b9ad8d9d-9827-44f9-9d2b-3f662c32eb9b">IBroadcastEventEx::FireEx</a>



<a href="https://msdn.microsoft.com/ab463f6e-0718-4420-89bc-28b3c447f3a0">IMSVidStreamBufferV2SourceEvent</a>
 

 

