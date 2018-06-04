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

# _EVT_RENDER_CONTEXT_FLAGS enumeration


## -description


Defines the values that specify the type of information to access from the event.


## -enum-fields




### -field EvtRenderContextValues

Render specific properties from the event.


### -field EvtRenderContextSystem

Render the system properties under the <b>System</b> element. The properties are returned in the order defined in the <a href="https://msdn.microsoft.com/a77cfbac-9abd-41e1-8ce6-ba92de97eb64">EVT_SYSTEM_PROPERTY_ID</a> enumeration.


### -field EvtRenderContextUser

Render all user-defined properties under the <b>UserData</b> or <b>EventData</b> element. If the data template associated with the event contains a <b>UserData</b> section, the <b>UserData</b> properties are rendered; otherwise, the <b>EventData</b> properties are rendered.


## -remarks



You cannot specify the EvtRenderContextValues flag with the EvtRenderContextSystem or EvtRenderContextUser flag.




## -see-also




<a href="https://msdn.microsoft.com/729cfd74-c158-463d-9247-ee2c75b259d4">EvtCreateRenderContext</a>
 

 

