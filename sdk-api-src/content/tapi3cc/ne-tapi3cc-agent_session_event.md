---
UID: NE:tapi3cc.AGENT_SESSION_EVENT
title: AGENT_SESSION_EVENT
author: windows-sdk-content
description: The AGENT_SESSION_EVENT enum describes agent session events. The ITAgentSessionEvent::get_Event method returns a member of this enum to indicate the type of agent session event that occurred.
old-location: tapi3\agent_session_event.htm
tech.root: tapi
ms.assetid: 44eb7669-6c0b-4b9c-a209-9f15f27a1ba9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AGENT_SESSION_EVENT, AGENT_SESSION_EVENT enumeration [TAPI 2.2], ASE_BUSY, ASE_END, ASE_NEW_SESSION, ASE_NOT_READY, ASE_READY, ASE_WRAPUP, _tapi3_agent_session_event, tapi3.agent_session_event, tapi3cc/AGENT_SESSION_EVENT, tapi3cc/ASE_BUSY, tapi3cc/ASE_END, tapi3cc/ASE_NEW_SESSION, tapi3cc/ASE_NOT_READY, tapi3cc/ASE_READY, tapi3cc/ASE_WRAPUP
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
 - AGENT_SESSION_EVENT
product: Windows
targetos: Windows
req.typenames: AGENT_SESSION_EVENT
req.redist: 
---

# AGENT_SESSION_EVENT enumeration


## -description


The 
<b>AGENT_SESSION_EVENT</b> enum describes agent session events. The 
<a href="https://msdn.microsoft.com/34779590-c2f6-4bd7-932b-5ac6365bcb20">ITAgentSessionEvent::get_Event</a> method returns a member of this enum to indicate the type of agent session event that occurred.


## -enum-fields




### -field ASE_NEW_SESSION

A new agent session has been created.


### -field ASE_NOT_READY

The agent is unable to handle calls for this session.


### -field ASE_READY

The agent is able to handle calls for this session.


### -field ASE_BUSY

The agent is active in this session handling an ACD call.


### -field ASE_WRAPUP

The agent is active in this session handling the wrap-up of an ACD call.


### -field ASE_END

The session has completed.


## -see-also




<a href="https://msdn.microsoft.com/34779590-c2f6-4bd7-932b-5ac6365bcb20">ITAgentSessionEvent::get_Event</a>



<a href="https://msdn.microsoft.com/d0ea4f7a-7b50-4610-ae17-957c0c1891e1">ITCallNotificationEvent</a>
 

 

