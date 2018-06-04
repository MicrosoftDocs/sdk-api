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

# lineagentgrouplist_tag structure


## -description


The 
<b>LINEAGENTGROUPLIST</b> structure describes a list of ACD agent groups. This structure can contain an array of 
<a href="https://msdn.microsoft.com/b1814ef7-7585-4203-8eb2-6862445f9114">LINEAGENTGROUPENTRY</a> structures.

Multiple functions use the 
<b>LINEAGENTGROUPLIST</b> structure; these include the 
<a href="https://msdn.microsoft.com/b3767efd-8f7a-4a03-81f6-97e11994900d">lineGetAgentGroupList</a>, 
<a href="https://msdn.microsoft.com/3e1d63e2-f87d-41ed-92ba-fe3bbdade8d3">lineGetGroupList</a> and 
<a href="https://msdn.microsoft.com/ce6795fb-fe11-4125-abeb-9b2686ea669a">lineSetAgentGroup</a> functions.


## -struct-fields




### -field dwTotalSize

Total size allocated to this data structure, in bytes.


### -field dwNeededSize

Size needed to hold all the information requested, in bytes.


### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.


### -field dwNumEntries

Number of 
<a href="https://msdn.microsoft.com/b1814ef7-7585-4203-8eb2-6862445f9114">LINEAGENTGROUPENTRY</a> structures that appear in the <i>List</i> array. The value is 0 if no agent is to be logged in on the address.


### -field dwListSize

Size of the group list array, in bytes.


### -field dwListOffset

Offset from the beginning of this structure to an array of 
<a href="https://msdn.microsoft.com/b1814ef7-7585-4203-8eb2-6862445f9114">LINEAGENTGROUPENTRY</a> structures that specify information about each group into which the current agent is to be logged in at the address. This is <b>dwNumEntries</b> times SIZEOF(LINEAGENTGROUPENTRY). The size of the field is specified by <b>dwListSize</b>.


## -see-also




<a href="https://msdn.microsoft.com/b1814ef7-7585-4203-8eb2-6862445f9114">LINEAGENTGROUPENTRY</a>



<a href="https://msdn.microsoft.com/b3767efd-8f7a-4a03-81f6-97e11994900d">lineGetAgentGroupList</a>



<a href="https://msdn.microsoft.com/3e1d63e2-f87d-41ed-92ba-fe3bbdade8d3">lineGetGroupList</a>



<a href="https://msdn.microsoft.com/ce6795fb-fe11-4125-abeb-9b2686ea669a">lineSetAgentGroup</a>
 

 

