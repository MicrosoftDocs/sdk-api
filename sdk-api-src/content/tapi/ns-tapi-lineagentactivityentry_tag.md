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

# lineagentactivityentry_tag structure


## -description


The 
<b>LINEAGENTACTIVITYENTRY</b> structure describes a single ACD agent activity. The 
<a href="https://msdn.microsoft.com/61e46717-8a14-440f-bb61-991c3dadd778">LINEAGENTACTIVITYLIST</a> structure can contain an array of 
<b>LINEAGENTACTIVITYENTRY</b> structures.


## -struct-fields




### -field dwID

Unique identifier for an activity. It is the responsibility of the agent handler to generate and maintain uniqueness of this identifier.


### -field dwNameSize

Size of the activity name including the <b>null</b> terminator, in bytes.


### -field dwNameOffset

Offset from the beginning of this structure to a <b>null</b>-terminated string specifying the name and other identifying information of an activity that can be selected by calling the 
<a href="https://msdn.microsoft.com/2c46e1cb-e2d7-4cb5-b937-55011058fd15">lineSetAgentActivity</a> function. The size of the string is specified by <b>dwNameSize</b>.


## -see-also




<a href="https://msdn.microsoft.com/61e46717-8a14-440f-bb61-991c3dadd778">LINEAGENTACTIVITYLIST</a>



<a href="https://msdn.microsoft.com/52c9b96e-4c59-46bf-ad37-78bcfc5e8dc3">LINEPROXYREQUEST</a>



<a href="https://msdn.microsoft.com/8f0be375-2891-45bd-a2cb-246ea5c4b9bb">lineGetAgentActivityList</a>



<a href="https://msdn.microsoft.com/2c46e1cb-e2d7-4cb5-b937-55011058fd15">lineSetAgentActivity</a>
 

 

