---
UID: NS:tapi.lineagentsessioninfo_tag
title: LINEAGENTSESSIONINFO (tapi.h)
description: The LINEAGENTSESSIONINFO structure contains information about the ACD agent session. The lineGetAgentSessionInfo function returns the LINEAGENTSESSIONINFO structure.
helpviewer_keywords: ["*LPLINEAGENTSESSIONINFO","LINEAGENTSESSIONINFO","LINEAGENTSESSIONINFO structure [TAPI 2.2]","LPLINEAGENTSESSIONINFO","LPLINEAGENTSESSIONINFO structure pointer [TAPI 2.2]","_tapi2_lineagentsessioninfo_str","tapi/LINEAGENTSESSIONINFO","tapi/LPLINEAGENTSESSIONINFO","tapi2.lineagentsessioninfo_str"]
old-location: tapi2\lineagentsessioninfo_str.htm
tech.root: tapi3
ms.assetid: 567e21b4-c79c-4a54-b9f4-6c8c949bf4ee
ms.date: 12/05/2018
ms.keywords: '*LPLINEAGENTSESSIONINFO, LINEAGENTSESSIONINFO, LINEAGENTSESSIONINFO structure [TAPI 2.2], LPLINEAGENTSESSIONINFO, LPLINEAGENTSESSIONINFO structure pointer [TAPI 2.2], _tapi2_lineagentsessioninfo_str, tapi/LINEAGENTSESSIONINFO, tapi/LPLINEAGENTSESSIONINFO, tapi2.lineagentsessioninfo_str'
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
req.typenames: LINEAGENTSESSIONINFO, *LPLINEAGENTSESSIONINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineagentsessioninfo_tag
 - tapi/lineagentsessioninfo_tag
 - LPLINEAGENTSESSIONINFO
 - tapi/LPLINEAGENTSESSIONINFO
 - LINEAGENTSESSIONINFO
 - tapi/LINEAGENTSESSIONINFO
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
 - LINEAGENTSESSIONINFO
---

# LINEAGENTSESSIONINFO structure


## -description

The 
<b>LINEAGENTSESSIONINFO</b> structure contains information about the ACD agent session. The 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetagentsessioninfo">lineGetAgentSessionInfo</a> function returns the 
<b>LINEAGENTSESSIONINFO</b> structure.

## -struct-fields

### -field dwTotalSize

Total size allocated to this structure, in bytes.

### -field dwNeededSize

Size needed to hold all the information requested, in bytes.

### -field dwUsedSize

Size of the portion of this structure that contains useful information, in bytes.

### -field dwAgentSessionState

One of the 
<a href="/windows/desktop/Tapi/lineagentsessionstate--constants">LINEAGENTSESSIONSTATE_ constants</a>.

### -field dwNextAgentSessionState

One of the 
<a href="/windows/desktop/Tapi/lineagentsessionstate--constants">LINEAGENTSESSIONSTATE_ constants</a>.

### -field dateSessionStartTime

Time session was created.

### -field dwSessionDuration

Duration of the agent session in seconds. Active period only; timing stops when a session enters the ASST_SESSION_ENDED state.

### -field dwNumberOfCalls

Number of ACD calls handled during this agent session by this agent.

### -field dwTotalTalkTime

Number of seconds spent talking in ACD calls during this agent session by this agent.

### -field dwAverageTalkTime

Average time spent talking for each ACD call during this agent session by this agent, in seconds.

### -field dwTotalCallTime

Number of seconds spent on ACD calls during this agent session by this agent. It includes time on the phone plus wrap-up time.

### -field dwAverageCallTime

Average time spent for each ACD call during this agent session, in seconds. Includes time on the phone plus wrap-up time.

### -field dwTotalWrapUpTime

Number of seconds spent on ACD call wrap-up (after-call work) during this agent session by this agent.

### -field dwAverageWrapUpTime

Average time for each ACD call spent in wrap-up (after-call work) during this agent session, in seconds.

### -field cyACDCallRate

Call rate for each agent session. This is a fixed-point decimal number.

### -field dwLongestTimeToAnswer

Longest time a call was waiting to be answered, in seconds.

### -field dwAverageTimeToAnswer

Average time calls waited to be answered, in seconds.

## -see-also

<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetagentsessioninfo">lineGetAgentSessionInfo</a>