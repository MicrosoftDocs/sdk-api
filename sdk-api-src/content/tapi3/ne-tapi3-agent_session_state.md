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

# AGENT_SESSION_STATE enumeration


## -description


This 
<b>AGENT_SESSION_STATE</b> enum defines the agent session indicators used by the 
<a href="https://msdn.microsoft.com/85a389ee-2d6c-4607-873a-8ca0c16a0fac">ITAgentSession::get_State</a> and the 
<a href="https://msdn.microsoft.com/4d35bacd-c4e4-4c31-b946-ad76ffb250ed">ITAgentSession::put_State</a> methods.


## -enum-fields




### -field ASST_NOT_READY

The agent is unable to handle calls for this session.


### -field ASST_READY

The agent is able to handle calls for this session.


### -field ASST_BUSY_ON_CALL

The agent is active in this session handling an ACD call.


### -field ASST_BUSY_WRAPUP

The agent is active in this session handling the wrap-up of an ACD call.


### -field ASST_SESSION_ENDED

The session has completed.


## -remarks



Following is a table of all valid AgentSession state transitions.

<table>
<tr>
<th>From state</th>
<th>To state</th>
</tr>
<tr>
<td>ASST_NOT_READY</td>
<td>
<dl>
<dt>ASST_READY</dt>
<dt>ASST_SESSION_ENDED</dt>
</dl>
</td>
</tr>
<tr>
<td>ASST_READY</td>
<td>
<dl>
<dt>ASST_BUSY_ON_CALL</dt>
<dt>ASST_NOT_READY</dt>
<dt>ASST_SESSION_ENDED</dt>
</dl>
</td>
</tr>
<tr>
<td>ASST_BUSY_ON_CALL</td>
<td>
<dl>
<dt>ASST_BUSY_WRAPUP</dt>
<dt>ASST_READY</dt>
<dt>ASST_NOT_READY</dt>
<dt>ASST_SESSION_ENDED</dt>
</dl>
</td>
</tr>
<tr>
<td>ASST_BUSY_WRAPUP</td>
<td>
<dl>
<dt>ASST_READY</dt>
<dt>ASST_NOT_READY</dt>
<dt>ASST_SESSION_ENDED</dt>
</dl>
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/85a389ee-2d6c-4607-873a-8ca0c16a0fac">ITAgentSession::get_State</a>



<a href="https://msdn.microsoft.com/4d35bacd-c4e4-4c31-b946-ad76ffb250ed">ITAgentSession::put_State</a>
 

 

