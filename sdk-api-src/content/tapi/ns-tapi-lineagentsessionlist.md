---
UID: NS:tapi.lineagentsessionlist_tag
title: LINEAGENTSESSIONLIST (tapi.h)
description: The LINEAGENTSESSIONLIST structure describes a list of ACD agent sessions. This structure can contain an array of LINEAGENTSESSIONENTRY structures. The lineGetAgentSessionList function returns the LINEAGENTSESSIONLIST structure.
old-location: tapi2\lineagentsessionlist_str.htm
tech.root: Tapi
ms.assetid: b14df70c-1630-46e7-a675-feb5c71dcd14
ms.date: 12/05/2018
ms.keywords: '*LPLINEAGENTSESSIONLIST, LINEAGENTSESSIONLIST, LINEAGENTSESSIONLIST structure [TAPI 2.2], LPLINEAGENTSESSIONLIST, LPLINEAGENTSESSIONLIST structure pointer [TAPI 2.2], _tapi2_lineagentsessionlist_str, tapi/LINEAGENTSESSIONLIST, tapi/LPLINEAGENTSESSIONLIST, tapi2.lineagentsessionlist_str'
f1_keywords:
- tapi/LINEAGENTSESSIONLIST
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
- LINEAGENTSESSIONLIST
targetos: Windows
req.typenames: LINEAGENTSESSIONLIST, *LPLINEAGENTSESSIONLIST
req.redist: 
ms.custom: 19H1
---

# LINEAGENTSESSIONLIST structure


## -description


The 
<b>LINEAGENTSESSIONLIST</b> structure describes a list of ACD agent sessions. This structure can contain an array of 
[LINEAGENTSESSIONENTRY](/windows/win32/api/tapi/ns-tapi-lineagentsessionentry)a> structures. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linegetagentsessionlist">lineGetAgentSessionList</a> function returns the 
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
[LINEAGENTSESSIONENTRY](/windows/win32/api/tapi/ns-tapi-lineagentsessionentry)a> structures that appear in the list array. The value is zero if no agent sessions have been created.


### -field dwListSize

Size of the agent session list array, in bytes.


### -field dwListOffset

Offset from the beginning of this structure to an array of 
[LINEAGENTSESSIONENTRY](/windows/win32/api/tapi/ns-tapi-lineagentsessionentry)a> structures that specify information about agents. The <b>dwListOffset</b> member is <b>dwNumEntries</b> times SIZEOF(LINEAGENTSESSIONENTRY). The size of the field is specified by <b>dwListSize</b>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



[LINEAGENTSESSIONENTRY](/windows/win32/api/tapi/ns-tapi-lineagentsessionentry)a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linegetagentsessionlist">lineGetAgentSessionList</a>
 

 

