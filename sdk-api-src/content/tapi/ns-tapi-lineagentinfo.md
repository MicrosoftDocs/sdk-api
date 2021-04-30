---
UID: NS:tapi.lineagentinfo_tag
title: LINEAGENTINFO (tapi.h)
description: The LINEAGENTINFO structure contains information about an ACD agent. The lineGetAgentInfo function returns the LINEAGENTINFO structure.
helpviewer_keywords: ["*LPLINEAGENTINFO","LINEAGENTINFO","LINEAGENTINFO structure [TAPI 2.2]","LPLINEAGENTINFO","LPLINEAGENTINFO structure pointer [TAPI 2.2]","_tapi2_lineagentinfo","tapi/LINEAGENTINFO","tapi/LPLINEAGENTINFO","tapi2.lineagentinfo"]
old-location: tapi2\lineagentinfo.htm
tech.root: tapi3
ms.assetid: 84eedf88-f0ea-4dc8-9840-b94a47fb7ca2
ms.date: 12/05/2018
ms.keywords: '*LPLINEAGENTINFO, LINEAGENTINFO, LINEAGENTINFO structure [TAPI 2.2], LPLINEAGENTINFO, LPLINEAGENTINFO structure pointer [TAPI 2.2], _tapi2_lineagentinfo, tapi/LINEAGENTINFO, tapi/LPLINEAGENTINFO, tapi2.lineagentinfo'
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
req.typenames: LINEAGENTINFO, *LPLINEAGENTINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineagentinfo_tag
 - tapi/lineagentinfo_tag
 - LPLINEAGENTINFO
 - tapi/LPLINEAGENTINFO
 - LINEAGENTINFO
 - tapi/LINEAGENTINFO
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
 - LINEAGENTINFO
---

# LINEAGENTINFO structure


## -description

The 
<b>LINEAGENTINFO</b> structure contains information about an ACD agent. The 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetagentinfo">lineGetAgentInfo</a> function returns the 
<b>LINEAGENTINFO</b> structure.

## -struct-fields

### -field dwTotalSize

Total size allocated to this structure including the null terminator, in bytes.

### -field dwNeededSize

Size needed to hold all the information requested, in bytes.

### -field dwUsedSize

Size of the portion of this structure that contains useful information, in bytes.

### -field dwAgentState

Must be one of the 
<a href="/windows/desktop/Tapi/lineagentstateex--constants">LINEAGENTSTATEEX_ constants</a>.

### -field dwNextAgentState

Must be one of the 
<a href="/windows/desktop/Tapi/lineagentstateex--constants">LINEAGENTSTATEEX_ constants</a>.

### -field dwMeasurementPeriod

Period for which the switch or implementation stores and calculates information, in seconds. For example, <b>dwNumberOfACDCalls</b> holds the number of calls the agent handled; <b>dwMeasurementPeriod</b> indicates if this value referenced the calls handed in the last hour, day, or month.

### -field cyOverallCallRate

Agent's call rate (calls per agent hour — where agent hour represents the time that an agent was active in one or more agent sessions) across all agent sessions. This is a fixed-point decimal number.

### -field dwNumberOfACDCalls

Number of ACD calls handled by this agent across all sessions.

### -field dwNumberOfIncomingCalls

Number of incoming non-ACD calls handled by this agent.

### -field dwNumberOfOutgoingCalls

Number of outgoing non-ACD calls handled by this agent.

### -field dwTotalACDTalkTime

Number of seconds spent talking in ACD calls by this agent across all sessions.

### -field dwTotalACDCallTime

Number of seconds spent on ACD calls by this agent (across all sessions). Includes the time on phone plus wrap-up time.

### -field dwTotalACDWrapUpTime

Number of seconds spent on ACD call wrap-up (after call work) by this agent across all sessions.

## -see-also

<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetagentinfo">lineGetAgentInfo</a>