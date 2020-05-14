---
UID: NF:segment.IMSVidStreamBufferSourceEvent3.BroadcastEventEx
title: IMSVidStreamBufferSourceEvent3::BroadcastEventEx (segment.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.helpviewer_keywords: ["BroadcastEventEx","BroadcastEventEx method [Microsoft TV Technologies]","BroadcastEventEx method [Microsoft TV Technologies]","IMSVidStreamBufferSourceEvent3 interface","IMSVidStreamBufferSourceEvent3 interface [Microsoft TV Technologies]","BroadcastEventEx method","IMSVidStreamBufferSourceEvent3.BroadcastEventEx","IMSVidStreamBufferSourceEvent3::BroadcastEventEx","IMSVidStreamBufferSourceEvent3BroadcastEventEx","mstv.imsvidstreambuffersourceevent3_broadcasteventex","segment/IMSVidStreamBufferSourceEvent3::BroadcastEventEx"]
old-location: mstv\imsvidstreambuffersourceevent3_broadcasteventex.htm
tech.root: mstv
ms.assetid: 2d97bcc0-ae13-436b-b741-2f22eb36f5de
ms.date: 12/05/2018
ms.keywords: BroadcastEventEx, BroadcastEventEx method [Microsoft TV Technologies], BroadcastEventEx method [Microsoft TV Technologies],IMSVidStreamBufferSourceEvent3 interface, IMSVidStreamBufferSourceEvent3 interface [Microsoft TV Technologies],BroadcastEventEx method, IMSVidStreamBufferSourceEvent3.BroadcastEventEx, IMSVidStreamBufferSourceEvent3::BroadcastEventEx, IMSVidStreamBufferSourceEvent3BroadcastEventEx, mstv.imsvidstreambuffersourceevent3_broadcasteventex, segment/IMSVidStreamBufferSourceEvent3::BroadcastEventEx
f1_keywords:
- segment/IMSVidStreamBufferSourceEvent3.BroadcastEventEx
dev_langs:
- c++
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
- IMSVidStreamBufferSourceEvent3.BroadcastEventEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidStreamBufferSourceEvent3::BroadcastEventEx


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>BroadcastEventEx</b> method is called when the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd695136(v=vs.85)">MSVidStreamBufferSource</a> object receives a broadcast event through the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ibroadcasteventex">IBroadcastEventEx</a> interface.


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



For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ibroadcasteventex-fireex">IBroadcastEventEx::FireEx</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidstreambuffersourceevent3">IMSVidStreamBufferSourceEvent3 Interface</a>
 

 

