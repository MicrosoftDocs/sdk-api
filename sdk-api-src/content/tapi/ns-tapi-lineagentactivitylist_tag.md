---
UID: NS:tapi.lineagentactivitylist_tag
title: lineagentactivitylist_tag
author: windows-sdk-content
description: The LINEAGENTACTIVITYLIST structure describes a list of ACD agent activities. This structure can contain an array of LINEAGENTACTIVITYENTRY structures. The lineGetAgentActivityList function returns the LINEAGENTACTIVITYLIST structure.
old-location: tapi2\lineagentactivitylist_str.htm
old-project: tapi
ms.assetid: 61e46717-8a14-440f-bb61-991c3dadd778
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: "*LPLINEAGENTACTIVITYLIST, LINEAGENTACTIVITYLIST, LINEAGENTACTIVITYLIST structure [TAPI 2.2], LPLINEAGENTACTIVITYLIST, LPLINEAGENTACTIVITYLIST structure pointer [TAPI 2.2], _tapi2_lineagentactivitylist_str, lineagentactivitylist_tag, tapi/LINEAGENTACTIVITYLIST, tapi/LPLINEAGENTACTIVITYLIST, tapi2.lineagentactivitylist_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tapi.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: LINEAGENTACTIVITYLIST, *LPLINEAGENTACTIVITYLIST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEAGENTACTIVITYLIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

