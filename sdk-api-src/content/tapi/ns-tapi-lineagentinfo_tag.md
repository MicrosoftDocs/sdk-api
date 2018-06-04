---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# lineagentinfo_tag structure


## -description


The 
<b>LINEAGENTINFO</b> structure contains information about an ACD agent. The 
<a href="https://msdn.microsoft.com/166b0595-2df0-431f-924c-6899b47408ac">lineGetAgentInfo</a> function returns the 
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
<a href="https://msdn.microsoft.com/d49025c5-f1db-4b71-a2d5-1cf3df66f3e5">LINEAGENTSTATEEX_ constants</a>.


### -field dwNextAgentState

Must be one of the 
<a href="https://msdn.microsoft.com/d49025c5-f1db-4b71-a2d5-1cf3df66f3e5">LINEAGENTSTATEEX_ constants</a>.


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




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/166b0595-2df0-431f-924c-6899b47408ac">lineGetAgentInfo</a>
 

 

