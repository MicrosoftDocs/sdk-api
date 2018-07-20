---
UID: NS:tapi.lineagentstatus_tag
title: lineagentstatus_tag
author: windows-sdk-content
description: The LINEAGENTSTATUS structure describes the current status of an ACD agent. The lineGetAgentStatus function returns the LINEAGENTSTATUS structure.
old-location: tapi2\lineagentstatus_str.htm
old-project: tapi
ms.assetid: c846bd16-79d2-4af0-b3ad-7432c28c542b
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: "*LPLINEAGENTSTATUS, LINEAGENTSTATUS, LINEAGENTSTATUS structure [TAPI 2.2], LPLINEAGENTSTATUS, LPLINEAGENTSTATUS structure pointer [TAPI 2.2], _tapi2_lineagentstatus_str, lineagentstatus_tag, tapi/LINEAGENTSTATUS, tapi/LPLINEAGENTSTATUS, tapi2.lineagentstatus_str"
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
tech.root: 
req.typenames: LINEAGENTSTATUS, *LPLINEAGENTSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEAGENTSTATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineagentstatus_tag structure


## -description


The 
<b>LINEAGENTSTATUS</b> structure describes the current status of an ACD agent. The 
<a href="https://msdn.microsoft.com/6736cde5-af38-493d-b09a-a807d9e9a382">lineGetAgentStatus</a> function returns the 
<b>LINEAGENTSTATUS</b> structure.


## -struct-fields




### -field dwTotalSize

Total size allocated to this data structure, in bytes. 


### -field dwNeededSize

Size needed to hold all the information requested, in bytes.


### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.


### -field dwNumEntries

Number of 
<a href="https://msdn.microsoft.com/b1814ef7-7585-4203-8eb2-6862445f9114">LINEAGENTGROUPENTRY</a> structures that appear in the <i>GroupList</i> array. The value is 0 if no agent is logged in on the address.


### -field dwGroupListSize

Size of the group list array, in bytes.


### -field dwGroupListOffset

Offset from the beginning of this structure to an array of 
<a href="https://msdn.microsoft.com/b1814ef7-7585-4203-8eb2-6862445f9114">LINEAGENTGROUPENTRY</a> structures. The size is <b>dwNumEntries</b> times SIZEOF(LINEAGENTGROUPENTRY). The array contains groups into which the agent is currently logged in on the address. The size of the field is specified by <b>dwGroupListSize</b>.


### -field dwState

Current state of the agent. One of the 
<a href="https://msdn.microsoft.com/1dbc33e7-05cc-4cb9-8904-f495b884b8db">LINEAGENTSTATE_ constants</a>.


### -field dwNextState

State into which the agent is automatically placed when the current call completes. One of the <a href="https://msdn.microsoft.com/1dbc33e7-05cc-4cb9-8904-f495b884b8db">LINEAGENTSTATE_ constants</a>.


### -field dwActivityID

Identifier of the current agent activity.


### -field dwActivitySize

Size of the agent activity string, in bytes.


### -field dwActivityOffset

Offset from the beginning of the structure to a null-terminated string specifying the current agent activity. The size of the string is specified by <b>dwActivitySize</b>.


### -field dwAgentFeatures

Agent-related features available at the time the status was obtained, using the 
<a href="https://msdn.microsoft.com/5953eb49-08ac-4c13-9fd3-df5473f96af8">LINEAGENTFEATURE_ constants</a>.


### -field dwValidStates

Agent states that could be selected, at this point in time, using 
<a href="https://msdn.microsoft.com/985798fd-54b1-4674-a1fe-b72c56c5176b">lineSetAgentState</a>. Consists of one or more of the 
<a href="https://msdn.microsoft.com/1dbc33e7-05cc-4cb9-8904-f495b884b8db">LINEAGENTSTATE_ constants</a>.


### -field dwValidNextStates

Next agent states that could be selected, at this point in time, by calling the 
<a href="https://msdn.microsoft.com/985798fd-54b1-4674-a1fe-b72c56c5176b">lineSetAgentState</a> function. Consists of one or more of the <a href="https://msdn.microsoft.com/1dbc33e7-05cc-4cb9-8904-f495b884b8db">LINEAGENTSTATE_ constants</a>.


## -see-also




<a href="https://msdn.microsoft.com/5953eb49-08ac-4c13-9fd3-df5473f96af8">LINEAGENTFEATURE_ constants</a>



<a href="https://msdn.microsoft.com/b1814ef7-7585-4203-8eb2-6862445f9114">LINEAGENTGROUPENTRY</a>



<a href="https://msdn.microsoft.com/1dbc33e7-05cc-4cb9-8904-f495b884b8db">LINEAGENTSTATE_ constants</a>



<a href="https://msdn.microsoft.com/6736cde5-af38-493d-b09a-a807d9e9a382">lineGetAgentStatus</a>



<a href="https://msdn.microsoft.com/985798fd-54b1-4674-a1fe-b72c56c5176b">lineSetAgentState</a>
 

 

