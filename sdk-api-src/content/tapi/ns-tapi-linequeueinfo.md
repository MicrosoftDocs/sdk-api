---
UID: NS:tapi.linequeueinfo_tag
title: LINEQUEUEINFO (tapi.h)
description: The LINEQUEUEINFO structure provides information about a queue on a line device. The lineGetQueueInfo function returns the LINEQUEUEINFO structure. This structure requires TAPI 3.0 version negotiation.
helpviewer_keywords: ["*LPLINEQUEUEINFO","LINEQUEUEINFO","LINEQUEUEINFO structure [TAPI 2.2]","LPLINEQUEUEINFO","LPLINEQUEUEINFO structure pointer [TAPI 2.2]","_tapi2_linequeueinfo","tapi/LINEQUEUEINFO","tapi/LPLINEQUEUEINFO","tapi2.linequeueinfo"]
old-location: tapi2\linequeueinfo.htm
tech.root: tapi3
ms.assetid: ba49404f-eb84-485f-be27-60760986d489
ms.date: 12/05/2018
ms.keywords: '*LPLINEQUEUEINFO, LINEQUEUEINFO, LINEQUEUEINFO structure [TAPI 2.2], LPLINEQUEUEINFO, LPLINEQUEUEINFO structure pointer [TAPI 2.2], _tapi2_linequeueinfo, tapi/LINEQUEUEINFO, tapi/LPLINEQUEUEINFO, tapi2.linequeueinfo'
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
targetos: Windows
req.typenames: LINEQUEUEINFO, *LPLINEQUEUEINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - linequeueinfo_tag
 - tapi/linequeueinfo_tag
 - LPLINEQUEUEINFO
 - tapi/LPLINEQUEUEINFO
 - LINEQUEUEINFO
 - tapi/LINEQUEUEINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEQUEUEINFO
---

# LINEQUEUEINFO structure


## -description

The 
<b>LINEQUEUEINFO</b> structure provides information about a queue on a line device. The 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetqueueinfo">lineGetQueueInfo</a> function returns the 
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

<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetqueueinfo">lineGetQueueInfo</a>