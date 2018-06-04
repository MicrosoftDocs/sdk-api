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

# lineagentsession_tag structure


## -description


The 
<b>LINEAGENTSESSIONENTRY</b> structure describes an ACD agent session. The 
<a href="https://msdn.microsoft.com/b14df70c-1630-46e7-a675-feb5c71dcd14">LINEAGENTSESSIONLIST</a> structure can contain an array of 
<b>LINEAGENTSESSIONENTRY</b> structures.


## -struct-fields




### -field hAgentSession

Unique identifier for an agent session. It is the responsibility of the agent handler to generate and maintain uniqueness of these identifiers.


### -field hAgent

Unique identifier for an agent. It is the responsibility of the agent handler to generate and maintain uniqueness of these identifiers.


### -field GroupID

Universally unique identifier for an ACD group. It is the responsibility of the agent handler to generate and maintain uniqueness of this identifier.


### -field dwWorkingAddressID

Address identifier on which the agent will receive calls for this session.


## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/b14df70c-1630-46e7-a675-feb5c71dcd14">LINEAGENTSESSIONLIST</a>



<a href="https://msdn.microsoft.com/6473d5dd-e08e-47f8-acad-b60943525b83">lineGetAgentSessionList</a>
 

 

