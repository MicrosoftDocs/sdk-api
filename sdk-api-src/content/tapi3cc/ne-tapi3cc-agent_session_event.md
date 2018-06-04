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
 

 

