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
 

 

