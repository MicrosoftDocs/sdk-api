---
UID: NF:segment.IMSVidStreamBufferSourceEvent3.BroadcastEventEx
title: IMSVidStreamBufferSourceEvent3::BroadcastEventEx
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\imsvidstreambuffersourceevent3_broadcasteventex.htm
old-project: mstv
ms.assetid: 2d97bcc0-ae13-436b-b741-2f22eb36f5de
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: BroadcastEventEx, BroadcastEventEx method [Microsoft TV Technologies], BroadcastEventEx method [Microsoft TV Technologies],IMSVidStreamBufferSourceEvent3 interface, IMSVidStreamBufferSourceEvent3 interface [Microsoft TV Technologies],BroadcastEventEx method, IMSVidStreamBufferSourceEvent3.BroadcastEventEx, IMSVidStreamBufferSourceEvent3::BroadcastEventEx, IMSVidStreamBufferSourceEvent3BroadcastEventEx, mstv.imsvidstreambuffersourceevent3_broadcasteventex, segment/IMSVidStreamBufferSourceEvent3::BroadcastEventEx
ms.prod: windows
ms.technology: windows-sdk
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
 - IMSVidStreamBufferSourceEvent3.BroadcastEventEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMSVidStreamBufferSourceEvent3::BroadcastEventEx


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>BroadcastEventEx</b> method is called when the <a href="https://msdn.microsoft.com/4043e199-d329-45f3-80a7-cd84fad88979">MSVidStreamBufferSource</a> object receives a broadcast event through the <a href="https://msdn.microsoft.com/c16ad538-afc6-4530-a2fd-18965b63983b">IBroadcastEventEx</a> interface.


## -parameters




### -param Guid [in]

GUID that specifies the event.


### -param Param1 [in]

First implementation-dependent parameter.


### -param Param2 [in]

Second implementation-dependent parameter.


### -param Param3 [in]

Third implementation-dependent parameter.


### -param Param4 [in]

Fourth implementation-dependent parameter.


## -returns



Return S_OK or an error code.




## -remarks



For more information, see <a href="https://msdn.microsoft.com/b9ad8d9d-9827-44f9-9d2b-3f662c32eb9b">IBroadcastEventEx::FireEx</a>.




## -see-also




<a href="https://msdn.microsoft.com/4ff2e05f-1c26-48f2-8c46-beebb8b0b1b3">IMSVidStreamBufferSourceEvent3 Interface</a>
 

 

