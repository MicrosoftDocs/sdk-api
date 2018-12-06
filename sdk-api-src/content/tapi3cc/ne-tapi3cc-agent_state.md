---
UID: NE:tapi3cc.AGENT_STATE
title: AGENT_STATE
author: windows-sdk-content
description: The AGENT_STATE enum is used by the ITAgent::put_State and ITAgent::get_State methods to describe the agent state.
old-location: tapi3\agent_state.htm
tech.root: tapi
ms.assetid: 6d63030e-cd47-48db-ab0d-a3c4f3aac733
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AGENT_STATE, AGENT_STATE enumeration [TAPI 2.2], AS_BUSY_ACD, AS_BUSY_INCOMING, AS_BUSY_OUTGOING, AS_NOT_READY, AS_READY, AS_UNKNOWN, _tapi3_agent_state, tapi3.agent_state, tapi3cc/AGENT_STATE, tapi3cc/AS_BUSY_ACD, tapi3cc/AS_BUSY_INCOMING, tapi3cc/AS_BUSY_OUTGOING, tapi3cc/AS_NOT_READY, tapi3cc/AS_READY, tapi3cc/AS_UNKNOWN
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tapi3cc.h
api_name:
 - AGENT_STATE
product: Windows
targetos: Windows
req.typenames: AGENT_STATE
req.redist: 
---

# AGENT_STATE enumeration


## -description


The 
<b>AGENT_STATE</b> enum is used by the 
<a href="https://msdn.microsoft.com/0f75146c-d8ce-4e9d-91bf-15dbb31b5c88">ITAgent::put_State</a> and 
<a href="https://msdn.microsoft.com/6690a62b-65a1-4892-aeee-4a6652939d5f">ITAgent::get_State</a> methods to describe the agent state.


## -enum-fields




### -field AS_NOT_READY

Agent is not ready


### -field AS_READY

Agent is ready


### -field AS_BUSY_ACD

Agent is busy with an ACD call.


### -field AS_BUSY_INCOMING

Agent has a call incoming.


### -field AS_BUSY_OUTGOING

Agent has a call that is outgoing.


### -field AS_UNKNOWN

Agent state unknown.


## -see-also




<a href="https://msdn.microsoft.com/6690a62b-65a1-4892-aeee-4a6652939d5f">ITAgent::get_State</a>



<a href="https://msdn.microsoft.com/0f75146c-d8ce-4e9d-91bf-15dbb31b5c88">ITAgent::put_State</a>
 

 

