---
UID: NS:tapi.lineagentsessioninfo_tag
title: lineagentsessioninfo_tag
author: windows-sdk-content
description: The LINEAGENTSESSIONINFO structure contains information about the ACD agent session. The lineGetAgentSessionInfo function returns the LINEAGENTSESSIONINFO structure.
old-location: tapi2\lineagentsessioninfo_str.htm
tech.root: Tapi
ms.assetid: 567e21b4-c79c-4a54-b9f4-6c8c949bf4ee
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*LPLINEAGENTSESSIONINFO, LINEAGENTSESSIONINFO, LINEAGENTSESSIONINFO structure [TAPI 2.2], LPLINEAGENTSESSIONINFO, LPLINEAGENTSESSIONINFO structure pointer [TAPI 2.2], _tapi2_lineagentsessioninfo_str, lineagentsessioninfo_tag, tapi/LINEAGENTSESSIONINFO, tapi/LPLINEAGENTSESSIONINFO, tapi2.lineagentsessioninfo_str"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - LINEAGENTSESSIONINFO
product: Windows
targetos: Windows
req.typenames: LINEAGENTSESSIONINFO, *LPLINEAGENTSESSIONINFO
req.redist: 
---

# lineagentsessioninfo_tag structure


## -description


The 
<b>LINEAGENTSESSIONINFO</b> structure contains information about the ACD agent session. The 
<a href="https://msdn.microsoft.com/06a5ea23-4205-46fd-abe7-ee4575be81c8">lineGetAgentSessionInfo</a> function returns the 
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
<a href="https://msdn.microsoft.com/8a0d06bb-51ba-4eaf-8719-120aed817f63">LINEAGENTSESSIONSTATE_ constants</a>.


### -field dwNextAgentSessionState

One of the 
<a href="https://msdn.microsoft.com/8a0d06bb-51ba-4eaf-8719-120aed817f63">LINEAGENTSESSIONSTATE_ constants</a>.


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




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/06a5ea23-4205-46fd-abe7-ee4575be81c8">lineGetAgentSessionInfo</a>
 

 

