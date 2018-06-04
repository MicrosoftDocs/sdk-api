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

# lineagentgroupentry_tag structure


## -description


The 
<b>LINEAGENTGROUPENTRY</b> structure provides information on ACD agent groups. The 
<a href="https://msdn.microsoft.com/6189eb8e-20a4-4c87-bc7f-0a6af9605be7">LINEAGENTGROUPLIST</a> structure can contain an array of 
<b>LINEAGENTGROUPENTRY</b> structures.


## -struct-fields




### -field GroupID


### -field GroupID.dwGroupID1

First part of the universally unique identifier for the group.


### -field GroupID.dwGroupID2

Second part of the universally unique identifier for the group.


### -field GroupID.dwGroupID3

Third part of the universally unique identifier for the group.


### -field GroupID.dwGroupID4

Fourth part of the universally unique identifier for a group. It is the responsibility of the agent handler to generate and maintain uniqueness of this identifier.


### -field dwNameSize

Size of the ACD group or queue name including the <b>null</b> terminator, in bytes.


### -field dwNameOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string specifying the name and other identifying information of an ACD group or queue into which the agent can log in. This string can contain such information as supervisor and skill level, to assist the agent in selecting the correct group from a list displayed on their workstation screen. The size of the field is specified by <b>dwNameSize</b>.


## -see-also




<a href="https://msdn.microsoft.com/6189eb8e-20a4-4c87-bc7f-0a6af9605be7">LINEAGENTGROUPLIST</a>



<a href="https://msdn.microsoft.com/b3767efd-8f7a-4a03-81f6-97e11994900d">lineGetAgentGroupList</a>



<a href="https://msdn.microsoft.com/3e1d63e2-f87d-41ed-92ba-fe3bbdade8d3">lineGetGroupList</a>



<a href="https://msdn.microsoft.com/ce6795fb-fe11-4125-abeb-9b2686ea669a">lineSetAgentGroup</a>
 

 

