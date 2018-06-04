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

# CALLHUB_EVENT enumeration


## -description


The 
<b>CALLHUB_EVENT</b> enum describes CallHub events. The 
<a href="https://msdn.microsoft.com/a2515583-e564-413d-b93f-6f2dd7776d7b">ITCallHubEvent::get_Event</a> method returns a member of this enum to indicate the type of CallHub event that occurred.


## -enum-fields




### -field CHE_CALLJOIN

A new call has joined the CallHub.


### -field CHE_CALLLEAVE

A call has left the CallHub.


### -field CHE_CALLHUBNEW

A new CallHub has appeared.


### -field CHE_CALLHUBIDLE

A CallHub has gone idle.


### -field CHE_LASTITEM




## -see-also




<a href="https://msdn.microsoft.com/a2515583-e564-413d-b93f-6f2dd7776d7b">ITCallHubEvent::get_Event</a>
 

 

