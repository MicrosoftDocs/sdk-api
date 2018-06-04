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

# lineagentsessionlist_tag structure


## -description


The 
<b>LINEAGENTSESSIONLIST</b> structure describes a list of ACD agent sessions. This structure can contain an array of 
<a href="https://msdn.microsoft.com/406b003a-11a2-445d-a466-a8549e201199">LINEAGENTSESSIONENTRY</a> structures. The 
<a href="https://msdn.microsoft.com/6473d5dd-e08e-47f8-acad-b60943525b83">lineGetAgentSessionList</a> function returns the 
<b>LINEAGENTSESSIONLIST</b> structure.


## -struct-fields




### -field dwTotalSize

Total size allocated to this structure, in bytes.


### -field dwNeededSize

Size needed to hold all the information requested, in bytes.


### -field dwUsedSize

Size of the portion of this structure that contains useful information, in bytes.


### -field dwNumEntries

Number of 
<a href="https://msdn.microsoft.com/406b003a-11a2-445d-a466-a8549e201199">LINEAGENTSESSIONENTRY</a> structures that appear in the list array. The value is zero if no agent sessions have been created.


### -field dwListSize

Size of the agent session list array, in bytes.


### -field dwListOffset

Offset from the beginning of this structure to an array of 
<a href="https://msdn.microsoft.com/406b003a-11a2-445d-a466-a8549e201199">LINEAGENTSESSIONENTRY</a> structures that specify information about agents. The <b>dwListOffset</b> member is <b>dwNumEntries</b> times SIZEOF(LINEAGENTSESSIONENTRY). The size of the field is specified by <b>dwListSize</b>.


## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/406b003a-11a2-445d-a466-a8549e201199">LINEAGENTSESSIONENTRY</a>



<a href="https://msdn.microsoft.com/6473d5dd-e08e-47f8-acad-b60943525b83">lineGetAgentSessionList</a>
 

 

