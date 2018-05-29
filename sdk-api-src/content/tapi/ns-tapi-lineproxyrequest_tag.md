---
UID: NS:tapi.lineproxyrequest_tag
title: lineproxyrequest_tag
author: windows-sdk-content
description: The LINEPROXYREQUEST structure contains parameter values of the application making the proxy request. Multiple TAPI call center functions generate a LINE_PROXYREQUEST message that references a LINEPROXYREQUEST structure.
old-location: tapi2\lineproxyrequest_str.htm
old-project: Tapi
ms.assetid: 52c9b96e-4c59-46bf-ad37-78bcfc5e8dc3
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*LPLINEPROXYREQUEST, LINEPROXYREQUEST, LINEPROXYREQUEST structure [TAPI 2.2], LPLINEPROXYREQUEST, LPLINEPROXYREQUEST structure pointer [TAPI 2.2], _tapi2_lineproxyrequest_str, lineproxyrequest_tag, tapi/LINEPROXYREQUEST, tapi/LPLINEPROXYREQUEST, tapi2.lineproxyrequest_str"
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
req.typenames: LINEPROXYREQUEST, *LPLINEPROXYREQUEST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tapi.h
api_name:
-	LINEPROXYREQUEST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineproxyrequest_tag structure


## -description


The 
<b>LINEPROXYREQUEST</b> structure contains parameter values of the application making the proxy request. Multiple 
<a href="https://msdn.microsoft.com/81bd0e7b-2bf1-4a05-83f4-ef641641cf2b">TAPI call center functions</a> generate a 
<a href="https://msdn.microsoft.com/7f33de55-2482-4558-bd86-ee2ac1e31269">LINE_PROXYREQUEST</a> message that references a 
<b>LINEPROXYREQUEST</b> structure.


## -struct-fields




### -field dwSize

Total number of bytes allocated by TAPI to contain the 
<b>LINEPROXYREQUEST</b> structure. The <b>dwTotalSize</b> member of any structure contained within 
<b>LINEPROXYREQUEST</b> (for example, 
<a href="https://msdn.microsoft.com/e4c5ece8-7b29-4154-9b38-f2b17049446f">LINEAGENTCAPS</a>) reflects only the number of bytes allocated for that specific structure.
Total size, in bytes, of the <i>Params</i> parameter block.


### -field dwClientMachineNameSize

Size of the client machine name string, in bytes, including the <b>null</b>-terminating character.


### -field dwClientMachineNameOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string identifying the client machine that made this request. The size of the string is specified by <b>dwClientMachineNameSize</b>.


### -field dwClientUserNameSize

Size of the client user name string, in bytes, including the <b>null</b>-terminating character.


### -field dwClientUserNameOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string identifying the user under whose account the application is running on the client machine. The size of the string is specified by <b>dwClientUserNameSize</b>.


### -field dwClientAppAPIVersion

Highest API version supported by the application that made the request. The proxy handler should restrict the contents of any data returned to the application to those members and values that were defined in this, or earlier, versions of TAPI.


### -field dwRequestType

One of the 
<a href="https://msdn.microsoft.com/5c05a567-cc65-411e-b049-919a442c5c57">LINEPROXYREQUEST_ Constants</a>. Identifies the type of function and the union component that defines the remaining data in the structure.


### -field SetAgentGroup

Union component used when <b>dwRequestType</b> is LINEPROXYREQUEST_SETAGENT. 





### -field SetAgentGroup.dwAddressID

Identifier of the address for which the agent is to be set.


### -field SetAgentGroup.GroupList

Structure of type 
<a href="https://msdn.microsoft.com/6189eb8e-20a4-4c87-bc7f-0a6af9605be7">LINEAGENTGROUPLIST</a>. Offsets within this structure are relative to the beginning of <b>SetAgentGroup.GroupList</b> rather than to the beginning of the 
<b>LINEPROXYREQUEST</b> structure.


### -field SetAgentState

Union component used when <b>dwRequestType</b> is LINEPROXYREQUEST_SETAGENTSTATE. 





### -field SetAgentState.dwAddressID

Identifier of the address for which the agent state is to be set.


### -field SetAgentState.dwAgentState

New agent state, or zero to leave the agent state unchanged.


### -field SetAgentState.dwNextAgentState

New next agent state, or zero to use the default next state associated with the specified agent state.


### -field SetAgentActivity

Union component used when <b>dwRequestType</b> is LINEPROXYREQUEST_SETAGENTACTIVITY. 





### -field SetAgentActivity.dwAddressID

Identifier of the address for which the agent activity is to be set.


### -field SetAgentActivity.dwActivityID

Identifier for the activity being selected.


### -field GetAgentCaps

Union component used when <b>dwRequestType</b> is LINEPROXYREQUEST_GETAGENTCAPS. 





### -field GetAgentCaps.dwAddressID

Identifier of the address for which the agent capabilities are to be retrieved.


### -field GetAgentCaps.AgentCaps

Structure of type 
<a href="https://msdn.microsoft.com/e4c5ece8-7b29-4154-9b38-f2b17049446f">LINEAGENTCAPS</a>. Offsets within this structure are relative to the beginning of <b>GetAgentCaps.AgentCaps</b> rather than to the beginning of the 
<b>LINEPROXYREQUEST</b> structure. The <b>dwTotalSize</b> member is set by TAPI and the remaining bytes set to zero. The proxy handler must fill in <b>dwNeededSize</b>, <b>dwUsedSize</b>, and the remaining members as appropriate, before calling 
<a href="https://msdn.microsoft.com/af774fc5-d013-4da2-a737-9e99c09456a0">lineProxyResponse</a>.


### -field GetAgentStatus

Union component used when <b>dwRequestType</b> is LINEPROXYREQUEST_SETAGENTGROUP. 





### -field GetAgentStatus.dwAddressID

Identifier of the address for which the agent status is to be retrieved.


### -field GetAgentStatus.AgentStatus

Structure of type 
<a href="https://msdn.microsoft.com/c846bd16-79d2-4af0-b3ad-7432c28c542b">LINEAGENTSTATUS</a>. Offsets within this structure are relative to the beginning of <b>GetAgentStatus.AgentStatus</b> rather than to the beginning of the 
<b>LINEPROXYREQUEST</b> structure. The <b>dwTotalSize</b> member is set by TAPI and the remaining bytes set to zero. The proxy handler must fill in <b>dwNeededSize</b>, <b>dwUsedSize</b>, and the remaining members as appropriate, before calling 
<a href="https://msdn.microsoft.com/af774fc5-d013-4da2-a737-9e99c09456a0">lineProxyResponse</a>.


### -field AgentSpecific

Union component used when <b>dwRequestType</b> is LINEPROXYREQUEST_AGENTSPECIFIC. 





### -field AgentSpecific.dwAddressID

Identifier of the address for which the agent status is to be retrieved.


### -field AgentSpecific.dwAgentExtensionIDIndex

Index of the handler extension being invoked; the identifier's position within the array of extension identifiers returned in 
<a href="https://msdn.microsoft.com/e4c5ece8-7b29-4154-9b38-f2b17049446f">LINEAGENTCAPS</a>.


### -field AgentSpecific.dwSize

Total size, in bytes, of the <i>Params</i> parameter block.


### -field AgentSpecific.Params

Block of memory that includes the contents passed to the handler from the application. If the handler is to return data to the application, it must be written into this parameter block before calling 
<a href="https://msdn.microsoft.com/af774fc5-d013-4da2-a737-9e99c09456a0">lineProxyResponse</a>.


### -field GetAgentActivityList

Union component used when <b>dwRequestType</b> is LINEPROXYREQUEST_GETAGENTACTIVITYLIST. 





### -field GetAgentActivityList.dwAddressID

Identifier of the address for which the agent activity list is to be retrieved.


### -field GetAgentActivityList.ActivityList

Structure of type 
<a href="https://msdn.microsoft.com/61e46717-8a14-440f-bb61-991c3dadd778">LINEAGENTACTIVITYLIST</a>. Offsets within this structure are relative to the beginning of <b>GetAgentActivityList.ActivityList</b> rather than to the beginning of the 
<b>LINEPROXYREQUEST</b> structure. The <b>dwTotalSize</b> member is set by TAPI and the remaining bytes set to zero. The proxy handler must fill in <b>dwNeededSize</b>, <b>dwUsedSize</b>, and the remaining members as appropriate, before calling 
<a href="https://msdn.microsoft.com/af774fc5-d013-4da2-a737-9e99c09456a0">lineProxyResponse</a>.


### -field GetAgentGroupList

Union component used when <b>dwRequestType</b> is LINEPROXYREQUEST_GETAGENTGROUPLIST. 





### -field GetAgentGroupList.dwAddressID

Identifier of the address for which the agent group list is to be retrieved.


### -field GetAgentGroupList.GroupList

Structure of type 
<a href="https://msdn.microsoft.com/6189eb8e-20a4-4c87-bc7f-0a6af9605be7">LINEAGENTGROUPLIST</a>. Offsets within this structure are relative to the beginning of <b>GetAgentGroupList.GroupList</b> rather than to the beginning of the 
<b>LINEPROXYREQUEST</b> structure. The <b>dwTotalSize</b> member is set by TAPI and the remaining bytes set to zero. The proxy handler must fill in <b>dwNeededSize</b>, <b>dwUsedSize</b>, and the remaining members as appropriate, before calling 
<a href="https://msdn.microsoft.com/af774fc5-d013-4da2-a737-9e99c09456a0">lineProxyResponse</a>.


### -field CreateAgent

Union component used when <b>dwRequestType</b> is LINEPROXYREQUEST_CREATEAGENT. 





### -field CreateAgent.hAgent

Unique identifier for an agent. It is the responsibility of the agent handler to generate and maintain uniqueness of this identifier.


### -field CreateAgent.dwAgentIDSize

Size of the agent ID string, in bytes.


### -field CreateAgent.dwAgentIDOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string that specifies the ID of the agent. The size of the string is specified by <b>dwAgentIDSize</b>.


### -field CreateAgent.dwAgentPINSize

Size of the PIN string including the <b>null</b> terminator, in bytes.


### -field CreateAgent.dwAgentPINOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string that specifies the PIN or password of the agent. The size of the string is specified by <b>dwAgentPINSize</b>.


### -field SetAgentStateEx

Union component used when <b>dwRequestType</b> is LINEPROXYREQUEST_SETAGENTSTATEEX. 





### -field SetAgentStateEx.hAgent

Unique identifier for an agent. It is the responsibility of the agent handler to generate and maintain uniqueness of this identifier.


### -field SetAgentStateEx.dwAgentState

One of the 
<a href="https://msdn.microsoft.com/d49025c5-f1db-4b71-a2d5-1cf3df66f3e5">LINEAGENTSTATEEX_ Constants</a>.


### -field SetAgentStateEx.dwNextAgentState

One of the 
<a href="https://msdn.microsoft.com/d49025c5-f1db-4b71-a2d5-1cf3df66f3e5">LINEAGENTSTATEEX_ Constants</a>.


### -field SetAgentMeasurementPeriod

Union component used when <b>dwRequestType</b> is LINEPROXYREQUEST_SETAGENTMEASUREMENTPERIOD. 





### -field SetAgentMeasurementPeriod.hAgent

Unique identifier for an agent. It is the responsibility of the agent handler to generate and maintain uniqueness of this identifier.


### -field SetAgentMeasurementPeriod.dwMeasurementPeriod

Period for which the switch or implementation stores and calculates information, in seconds. For example, <b>dwNumberOfACDCalls</b> holds the number of calls the agent handled; <b>dwMeasurementPeriod</b> indicates if this value referenced the calls handled in the last hour, day, or month.


### -field GetAgentInfo

Union component used when <b>dwRequestType</b> is LINEPROXYREQUEST_GETAGENTINFO. 





### -field GetAgentInfo.hAgent

Unique identifier for an agent. It is the responsibility of the agent handler to generate and maintain uniqueness of this identifier.


### -field GetAgentInfo.AgentInfo

Structure of type 
<a href="https://msdn.microsoft.com/84eedf88-f0ea-4dc8-9840-b94a47fb7ca2">LINEAGENTINFO</a>.


### -field CreateAgentSession

Union component used when <b>dwRequestType</b> is LINEPROXYREQUEST_CREATEAGENTSESSION. 





### -field CreateAgentSession.hAgentSession

Unique identifier for an agent session.


### -field CreateAgentSession.dwAgentPINSize

Size of the agent PIN string including the <b>null</b> terminator, in bytes.


### -field CreateAgentSession.dwAgentPINOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string that specifies the PIN or password of the agent. The size of this string is specified by <b>dwAgentPINSize</b>.


### -field CreateAgentSession.hAgent

Unique identifier for an agent. It is the responsibility of the agent handler to generate and maintain uniqueness of this identifier.


### -field CreateAgentSession.GroupID

Universally unique identifier for an ACD group. It is the responsibility of the agent handler to generate and maintain uniqueness of this identifier.


### -field CreateAgentSession.dwWorkingAddressID

Identifier of the address on which the agent will receive calls for this session.


### -field GetAgentSessionList

Union component used when <b>dwRequestType</b> is LINEPROXYREQUEST_GETAGENTSESSIONLIST. 





### -field GetAgentSessionList.hAgent

Unique identifier for an agent. It is the responsibility of the agent handler to generate and maintain uniqueness of this identifier.


### -field GetAgentSessionList.SessionList

Structure of type 
<a href="https://msdn.microsoft.com/b14df70c-1630-46e7-a675-feb5c71dcd14">LINEAGENTSESSIONLIST</a>.


### -field GetAgentSessionInfo

Union component used when <b>dwRequestType</b> is LINEPROXYREQUEST_GETAGENTSESSIONINFO. 





### -field GetAgentSessionInfo.hAgentSession

Unique identifier for an agent session. It is the responsibility of the agent handler to generate and maintain uniqueness of this identifier.


### -field GetAgentSessionInfo.SessionInfo

Structure of type 
<a href="https://msdn.microsoft.com/567e21b4-c79c-4a54-b9f4-6c8c949bf4ee">LINEAGENTSESSIONINFO</a>.


### -field SetAgentSessionState

Union component used when <b>dwRequestType</b> is LINEPROXYREQUEST_SETAGENTSESSIONSTATE. 





### -field SetAgentSessionState.hAgentSession

Unique identifier for an agent session. It is the responsibility of the agent handler to generate and maintain uniqueness of this identifier.


### -field SetAgentSessionState.dwAgentSessionState

One of the 
<a href="https://msdn.microsoft.com/8a0d06bb-51ba-4eaf-8719-120aed817f63">LINEAGENTSESSIONSTATE_ constants</a>.


### -field SetAgentSessionState.dwNextAgentSessionState

One of the 
<a href="https://msdn.microsoft.com/8a0d06bb-51ba-4eaf-8719-120aed817f63">LINEAGENTSESSIONSTATE_ constants</a>.


### -field GetQueueList

Union component used when <b>dwRequestType</b> is LINEPROXYREQUEST_GETQUEUELIST. 





### -field GetQueueList.GroupID

Universally unique identifier for an ACD group. It is the responsibility of the agent handler to generate and maintain uniqueness of this identifier.


### -field GetQueueList.QueueList

Structure of type 
<a href="https://msdn.microsoft.com/86645d7c-f683-48e7-8342-3e9d5961913a">LINEQUEUELIST</a>.


### -field SetQueueMeasurementPeriod

Union component used when <b>dwRequestType</b> is LINEPROXYREQUEST_SETQUEUEMEASUREMENTPERIOD. 





### -field SetQueueMeasurementPeriod.dwQueueID

Unique identifier for a queue. It is the responsibility of the agent handler to generate and maintain uniqueness of this identifier.


### -field SetQueueMeasurementPeriod.dwMeasurementPeriod

Period for which the switch or implementation stores and calculates information, in seconds.


### -field GetQueueInfo

Union component used when <b>dwRequestType</b> is LINEPROXYREQUEST_GETQUEUEINFO. 





### -field GetQueueInfo.dwQueueID

Unique identifier for a queue. It is the responsibility of the agent handler to generate and maintain uniqueness of this identifier.


### -field GetQueueInfo.QueueInfo

Structure of type 
<a href="https://msdn.microsoft.com/ba49404f-eb84-485f-be27-60760986d489">LINEQUEUEINFO</a>.


### -field GetGroupList

Union component used when <b>dwRequestType</b> is LINEPROXYREQUEST_GETGROUPLIST. 





### -field GetGroupList.GroupList

Structure of type 
<a href="https://msdn.microsoft.com/6189eb8e-20a4-4c87-bc7f-0a6af9605be7">LINEAGENTGROUPLIST</a>.


## -remarks



An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.




## -see-also




<a href="https://msdn.microsoft.com/61e46717-8a14-440f-bb61-991c3dadd778">LINEAGENTACTIVITYLIST</a>



<a href="https://msdn.microsoft.com/e4c5ece8-7b29-4154-9b38-f2b17049446f">LINEAGENTCAPS</a>



<a href="https://msdn.microsoft.com/6189eb8e-20a4-4c87-bc7f-0a6af9605be7">LINEAGENTGROUPLIST</a>



<a href="https://msdn.microsoft.com/567e21b4-c79c-4a54-b9f4-6c8c949bf4ee">LINEAGENTSESSIONINFO</a>



<a href="https://msdn.microsoft.com/b14df70c-1630-46e7-a675-feb5c71dcd14">LINEAGENTSESSIONLIST</a>



<a href="https://msdn.microsoft.com/c846bd16-79d2-4af0-b3ad-7432c28c542b">LINEAGENTSTATUS</a>



<a href="https://msdn.microsoft.com/86645d7c-f683-48e7-8342-3e9d5961913a">LINEQUEUELIST</a>



<a href="https://msdn.microsoft.com/7f33de55-2482-4558-bd86-ee2ac1e31269">LINE_PROXYREQUEST</a>



<a href="https://msdn.microsoft.com/af774fc5-d013-4da2-a737-9e99c09456a0">lineProxyResponse</a>
 

 

