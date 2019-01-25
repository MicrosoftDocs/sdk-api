---
UID: NE:tapi3.AGENT_EVENT
title: AGENT_EVENT
author: windows-sdk-content
description: The AGENT_EVENT enum describes agent events. The ITAgentEvent::get_Event method returns a member of this enum to indicate the type of agent event that occurred.
old-location: tapi3\agent_event.htm
tech.root: Tapi
ms.assetid: 9dec832a-98da-436a-89c8-d5c69053082a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AE_BUSY_ACD, AE_BUSY_INCOMING, AE_BUSY_OUTGOING, AE_NOT_READY, AE_READY, AE_UNKNOWN, AGENT_EVENT, AGENT_EVENT enumeration [TAPI 2.2], _tapi3_agent_event, tapi3.agent_event, tapi3cc/AE_BUSY_ACD, tapi3cc/AE_BUSY_INCOMING, tapi3cc/AE_BUSY_OUTGOING, tapi3cc/AE_NOT_READY, tapi3cc/AE_READY, tapi3cc/AE_UNKNOWN, tapi3cc/AGENT_EVENT
ms.topic: enum
req.header: tapi3.h
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
 - AGENT_EVENT
product: Windows
targetos: Windows
req.typenames: AGENT_EVENT
req.redist: 
---

# AGENT_EVENT enumeration


## -description


The 
<b>AGENT_EVENT</b> enum describes agent events. The 
<a href="https://msdn.microsoft.com/d402b2b4-2817-4ebe-b735-69ea9e975f54">ITAgentEvent::get_Event</a> method returns a member of this enum to indicate the type of agent event that occurred.


## -enum-fields




### -field AE_NOT_READY

The agent is unable to handle calls.


### -field AE_READY

The agent is able to handle calls.


### -field AE_BUSY_ACD

The agent is active handling an ACD call.


### -field AE_BUSY_INCOMING

The agent is active handling an incoming non-ACD call.


### -field AE_BUSY_OUTGOING

The agent is active handling an outgoing non-ACD call.


### -field AE_UNKNOWN

Unknown state.


## -see-also




<a href="https://msdn.microsoft.com/d402b2b4-2817-4ebe-b735-69ea9e975f54">ITAgentEvent::get_Event</a>



<a href="https://msdn.microsoft.com/d0ea4f7a-7b50-4610-ae17-957c0c1891e1">ITCallNotificationEvent</a>
 

 

