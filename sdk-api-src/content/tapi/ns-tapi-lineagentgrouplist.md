---
UID: NS:tapi.lineagentgrouplist_tag
title: LINEAGENTGROUPLIST (tapi.h)
description: The LINEAGENTGROUPLIST structure describes a list of ACD agent groups. This structure can contain an array of LINEAGENTGROUPENTRY structures.
helpviewer_keywords: ["*LPLINEAGENTGROUPLIST","LINEAGENTGROUPLIST","LINEAGENTGROUPLIST structure [TAPI 2.2]","LPLINEAGENTGROUPLIST","LPLINEAGENTGROUPLIST structure pointer [TAPI 2.2]","_tapi2_lineagentgrouplist_str","tapi/LINEAGENTGROUPLIST","tapi/LPLINEAGENTGROUPLIST","tapi2.lineagentgrouplist_str"]
old-location: tapi2\lineagentgrouplist_str.htm
tech.root: tapi3
ms.assetid: 6189eb8e-20a4-4c87-bc7f-0a6af9605be7
ms.date: 12/05/2018
ms.keywords: '*LPLINEAGENTGROUPLIST, LINEAGENTGROUPLIST, LINEAGENTGROUPLIST structure [TAPI 2.2], LPLINEAGENTGROUPLIST, LPLINEAGENTGROUPLIST structure pointer [TAPI 2.2], _tapi2_lineagentgrouplist_str, tapi/LINEAGENTGROUPLIST, tapi/LPLINEAGENTGROUPLIST, tapi2.lineagentgrouplist_str'
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
targetos: Windows
req.typenames: LINEAGENTGROUPLIST, *LPLINEAGENTGROUPLIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineagentgrouplist_tag
 - tapi/lineagentgrouplist_tag
 - LPLINEAGENTGROUPLIST
 - tapi/LPLINEAGENTGROUPLIST
 - LINEAGENTGROUPLIST
 - tapi/LINEAGENTGROUPLIST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEAGENTGROUPLIST
---

# LINEAGENTGROUPLIST structure


## -description

The 
<b>LINEAGENTGROUPLIST</b> structure describes a list of ACD agent groups. This structure can contain an array of 
<a href="/windows/desktop/api/tapi/ns-tapi-lineagentgroupentry">LINEAGENTGROUPENTRY</a> structures.

Multiple functions use the 
<b>LINEAGENTGROUPLIST</b> structure; these include the 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetagentgrouplista">lineGetAgentGroupList</a>, 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetgrouplista">lineGetGroupList</a> and 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetagentgroup">lineSetAgentGroup</a> functions.

## -struct-fields

### -field dwTotalSize

Total size allocated to this data structure, in bytes.

### -field dwNeededSize

Size needed to hold all the information requested, in bytes.

### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.

### -field dwNumEntries

Number of 
<a href="/windows/desktop/api/tapi/ns-tapi-lineagentgroupentry">LINEAGENTGROUPENTRY</a> structures that appear in the <i>List</i> array. The value is 0 if no agent is to be logged in on the address.

### -field dwListSize

Size of the group list array, in bytes.

### -field dwListOffset

Offset from the beginning of this structure to an array of 
<a href="/windows/desktop/api/tapi/ns-tapi-lineagentgroupentry">LINEAGENTGROUPENTRY</a> structures that specify information about each group into which the current agent is to be logged in at the address. This is <b>dwNumEntries</b> times SIZEOF(LINEAGENTGROUPENTRY). The size of the field is specified by <b>dwListSize</b>.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-lineagentgroupentry">LINEAGENTGROUPENTRY</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetagentgrouplista">lineGetAgentGroupList</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetgrouplista">lineGetGroupList</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetagentgroup">lineSetAgentGroup</a>