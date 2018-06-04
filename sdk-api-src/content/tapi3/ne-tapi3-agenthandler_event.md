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

# AGENTHANDLER_EVENT enumeration


## -description


The 
<b>AGENTHANDLER_EVENT</b> enum describes agent handler events. The 
<a href="https://msdn.microsoft.com/3362964c-15d3-497c-876b-46e8d26389c0">ITAgentHandlerEvent::get_Event</a> method returns a member of this enum to indicate the type of agent handler event that occurred.


## -enum-fields




### -field AHE_NEW_AGENTHANDLER

A new AgentHandler object has been added.


### -field AHE_AGENTHANDLER_REMOVED

An AgentHandler object has been removed.


## -see-also




<a href="https://msdn.microsoft.com/3362964c-15d3-497c-876b-46e8d26389c0">ITAgentHandlerEvent::get_Event</a>



<a href="https://msdn.microsoft.com/d0ea4f7a-7b50-4610-ae17-957c0c1891e1">ITCallNotificationEvent</a>
 

 

