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

# lineagententry_tag structure


## -description


The 
<b>LINEAGENTENTRY</b> structure describes an individual ACD agent. The 
<a href="https://msdn.microsoft.com/176beb90-a9aa-4d40-9f84-e6ea9f84b5a2">LINEAGENTLIST</a> structure can contain an array of 
<b>LINEAGENTENTRY</b> structures.


## -struct-fields




### -field hAgent

Unique identifier for an agent. It is the responsibility of the agent handler to generate and maintain uniqueness of these identifiers.


### -field dwNameSize

Size of the agent name string including the <b>null</b> terminator, in bytes. 


### -field dwNameOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string that specifies the name of the agent, which is also the operating system's user name. The size of the string is specified by <b>dwNameSize</b>.


### -field dwIDSize

Size of the ID string including the <b>null</b> terminator, in bytes.


### -field dwIDOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string that specifies the ID of the agent. Used by legacy ACD systems to identify the agent. The size of the string is specified by <b>dwIDSize</b>.


### -field dwPINSize

Size of the PIN string, in bytes.


### -field dwPINOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string that specifies the PIN or password of the agent. Used by legacy ACD systems for agent authorization. The size of the string is specified by <b>dwPINSize</b>.


## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/176beb90-a9aa-4d40-9f84-e6ea9f84b5a2">LINEAGENTLIST</a>
 

 

