---
UID: NS:tapi.lineagentactivitylist_tag
title: LINEAGENTACTIVITYLIST (tapi.h)
description: The LINEAGENTACTIVITYLIST structure describes a list of ACD agent activities. This structure can contain an array of LINEAGENTACTIVITYENTRY structures. The lineGetAgentActivityList function returns the LINEAGENTACTIVITYLIST structure.helpviewer_keywords: ["*LPLINEAGENTACTIVITYLIST","LINEAGENTACTIVITYLIST","LINEAGENTACTIVITYLIST structure [TAPI 2.2]","LPLINEAGENTACTIVITYLIST","LPLINEAGENTACTIVITYLIST structure pointer [TAPI 2.2]","_tapi2_lineagentactivitylist_str","tapi/LINEAGENTACTIVITYLIST","tapi/LPLINEAGENTACTIVITYLIST","tapi2.lineagentactivitylist_str"]
old-location: tapi2\lineagentactivitylist_str.htm
tech.root: Tapi
ms.assetid: 61e46717-8a14-440f-bb61-991c3dadd778
ms.date: 12/05/2018
ms.keywords: '*LPLINEAGENTACTIVITYLIST, LINEAGENTACTIVITYLIST, LINEAGENTACTIVITYLIST structure [TAPI 2.2], LPLINEAGENTACTIVITYLIST, LPLINEAGENTACTIVITYLIST structure pointer [TAPI 2.2], _tapi2_lineagentactivitylist_str, tapi/LINEAGENTACTIVITYLIST, tapi/LPLINEAGENTACTIVITYLIST, tapi2.lineagentactivitylist_str'
f1_keywords:
- tapi/LINEAGENTACTIVITYLIST
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Tapi.h
api_name:
- LINEAGENTACTIVITYLIST
targetos: Windows
req.typenames: LINEAGENTACTIVITYLIST, *LPLINEAGENTACTIVITYLIST
req.redist: 
ms.custom: 19H1
---

# LINEAGENTACTIVITYLIST structure


## -description


The 
<b>LINEAGENTACTIVITYLIST</b> structure describes a list of ACD agent activities. This structure can contain an array of 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-lineagentactivityentry">LINEAGENTACTIVITYENTRY</a> structures. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linegetagentactivitylista">lineGetAgentActivityList</a> function returns the 
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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-lineagentactivityentry">LINEAGENTACTIVITYENTRY</a> structures that appear in the <i>List</i> array. The value is 0 if no agent activity codes are available.


### -field dwListSize

Size of the activity list array, in bytes.


### -field dwListOffset

Offset from the beginning of the structure to an array of 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-lineagentactivityentry">LINEAGENTACTIVITYENTRY</a> structures indicating information about activity that could be specified for the current logged-in agent. This is <b>dwNumEntries</b> times SIZEOF(LINEAGENTACTIVITYENTRY). The size of the array is specified by <b>dwListSize</b>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-lineagentactivityentry">LINEAGENTACTIVITYENTRY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linegetagentactivitylista">lineGetAgentActivityList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linesetagentactivity">lineSetAgentActivity</a>
 

 

