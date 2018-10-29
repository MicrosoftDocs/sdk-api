---
UID: NS:tapi.lineagentsessionlist_tag
title: lineagentsessionlist_tag
author: windows-sdk-content
description: The LINEAGENTSESSIONLIST structure describes a list of ACD agent sessions. This structure can contain an array of LINEAGENTSESSIONENTRY structures. The lineGetAgentSessionList function returns the LINEAGENTSESSIONLIST structure.
old-location: tapi2\lineagentsessionlist_str.htm
tech.root: Tapi
ms.assetid: b14df70c-1630-46e7-a675-feb5c71dcd14
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*LPLINEAGENTSESSIONLIST, LINEAGENTSESSIONLIST, LINEAGENTSESSIONLIST structure [TAPI 2.2], LPLINEAGENTSESSIONLIST, LPLINEAGENTSESSIONLIST structure pointer [TAPI 2.2], _tapi2_lineagentsessionlist_str, lineagentsessionlist_tag, tapi/LINEAGENTSESSIONLIST, tapi/LPLINEAGENTSESSIONLIST, tapi2.lineagentsessionlist_str"
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
 - LINEAGENTSESSIONLIST
product: Windows
targetos: Windows
req.typenames: LINEAGENTSESSIONLIST, *LPLINEAGENTSESSIONLIST
req.redist: 
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
 

 

