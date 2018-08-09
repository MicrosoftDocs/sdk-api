---
UID: NE:tapi3cc.AGENT_SESSION_STATE
title: AGENT_SESSION_STATE
author: windows-sdk-content
description: This AGENT_SESSION_STATE enum defines the agent session indicators used by the ITAgentSession::get_State and the ITAgentSession::put_State methods.
old-location: tapi3\agent_session_state.htm
old-project: tapi
ms.assetid: 0c902924-e142-4ab9-9b20-661d7c2e3629
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: AGENT_SESSION_STATE, AGENT_SESSION_STATE enumeration [TAPI 2.2], ASST_BUSY_ON_CALL, ASST_BUSY_WRAPUP, ASST_NOT_READY, ASST_READY, ASST_SESSION_ENDED, _tapi3_agent_session_state, tapi3.agent_session_state, tapi3cc/AGENT_SESSION_STATE, tapi3cc/ASST_BUSY_ON_CALL, tapi3cc/ASST_BUSY_WRAPUP, tapi3cc/ASST_NOT_READY, tapi3cc/ASST_READY, tapi3cc/ASST_SESSION_ENDED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: tapi3cc.h
req.include-header: Tapi3.h
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
req.typenames: AGENT_SESSION_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tapi3cc.h
api_name:
 - AGENT_SESSION_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

