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

# lineagentactivitylist_tag structure


## -description


The 
<b>LINEAGENTACTIVITYLIST</b> structure describes a list of ACD agent activities. This structure can contain an array of 
<a href="https://msdn.microsoft.com/e4f869a9-608c-4119-863b-b29e8b0d9680">LINEAGENTACTIVITYENTRY</a> structures. The 
<a href="https://msdn.microsoft.com/8f0be375-2891-45bd-a2cb-246ea5c4b9bb">lineGetAgentActivityList</a> function returns the 
<b>LINEAGENTACTIVITYLIST</b> structure.


## -struct-fields




### -field dwTotalSize

Total size allocated to this data structure, in bytes.


### -field dwNeededSize

Size needed to hold all the information requested, in bytes.


### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.


### -field dwNumEntries

Number of 
<a href="https://msdn.microsoft.com/e4f869a9-608c-4119-863b-b29e8b0d9680">LINEAGENTACTIVITYENTRY</a> structures that appear in the <i>List</i> array. The value is 0 if no agent activity codes are available.


### -field dwListSize

Size of the activity list array, in bytes.


### -field dwListOffset

Offset from the beginning of the structure to an array of 
<a href="https://msdn.microsoft.com/e4f869a9-608c-4119-863b-b29e8b0d9680">LINEAGENTACTIVITYENTRY</a> structures indicating information about activity that could be specified for the current logged-in agent. This is <b>dwNumEntries</b> times SIZEOF(LINEAGENTACTIVITYENTRY). The size of the array is specified by <b>dwListSize</b>.


## -see-also




<a href="https://msdn.microsoft.com/e4f869a9-608c-4119-863b-b29e8b0d9680">LINEAGENTACTIVITYENTRY</a>



<a href="https://msdn.microsoft.com/8f0be375-2891-45bd-a2cb-246ea5c4b9bb">lineGetAgentActivityList</a>



<a href="https://msdn.microsoft.com/2c46e1cb-e2d7-4cb5-b937-55011058fd15">lineSetAgentActivity</a>
 

 

