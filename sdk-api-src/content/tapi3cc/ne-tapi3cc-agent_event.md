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
 

 

