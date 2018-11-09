---
UID: NS:tapi.linequeueinfo_tag
title: linequeueinfo_tag
author: windows-sdk-content
description: The LINEQUEUEINFO structure provides information about a queue on a line device. The lineGetQueueInfo function returns the LINEQUEUEINFO structure. This structure requires TAPI 3.0 version negotiation.
old-location: tapi2\linequeueinfo.htm
tech.root: tapi
ms.assetid: ba49404f-eb84-485f-be27-60760986d489
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "*LPLINEQUEUEINFO, LINEQUEUEINFO, LINEQUEUEINFO structure [TAPI 2.2], LPLINEQUEUEINFO, LPLINEQUEUEINFO structure pointer [TAPI 2.2], _tapi2_linequeueinfo, linequeueinfo_tag, tapi/LINEQUEUEINFO, tapi/LPLINEQUEUEINFO, tapi2.linequeueinfo"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEQUEUEINFO
product: Windows
targetos: Windows
req.typenames: LINEQUEUEINFO, *LPLINEQUEUEINFO
req.redist: 
---

# linequeueinfo_tag structure


## -description


The 
<b>LINEQUEUEINFO</b> structure provides information about a queue on a line device. The 
<a href="https://msdn.microsoft.com/f7bd6922-a9cd-43ab-96f7-5abf4c6a5b16">lineGetQueueInfo</a> function returns the 
<b>LINEQUEUEINFO</b> structure. This structure requires TAPI 3.0 version negotiation.


## -struct-fields




### -field dwTotalSize

Total size allocated to this structure, in bytes.


### -field dwNeededSize

Size needed to hold all the information requested, in bytes.


### -field dwUsedSize

Size of the portion of this structure that contains useful information, in bytes.


### -field dwMeasurementPeriod

Period for which the switch or implementation stores and calculates information, in seconds. For example, <b>dwTotalCallsAbandoned</b> holds the number of abandoned calls; <b>dwMeasurementPeriod</b> would indicate if this value referenced the calls queued in an hour, day, or month, for example.


### -field dwTotalCallsQueued

Total number of incoming calls for this queue during this measurement period.


### -field dwCurrentCallsQueued

Number of incoming calls currently waiting.


### -field dwTotalCallsAbandoned

Number of abandoned calls during this measurement period.


### -field dwTotalCallsFlowedIn

Total number of calls that flowed into this queue (passed down from another queue or ACD group) during this measurement period.


### -field dwTotalCallsFlowedOut

Total number of calls that flowed out of this queue (passed down to another queue or ACD group) during this measurement period.


### -field dwLongestEverWaitTime

Longest time any call has waited in queue, in seconds.


### -field dwCurrentLongestWaitTime

Longest time that a current call (call still in queue) has been waiting, in seconds.


### -field dwAverageWaitTime

Average time that a call has waited in queue, in seconds.


### -field dwFinalDisposition

Final disposition of the queue.


## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/f7bd6922-a9cd-43ab-96f7-5abf4c6a5b16">lineGetQueueInfo</a>
 

 

