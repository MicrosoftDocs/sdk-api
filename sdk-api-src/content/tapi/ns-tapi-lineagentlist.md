---
UID: NS:tapi.lineagentlist_tag
title: LINEAGENTLIST (tapi.h)
description: The LINEAGENTLIST structure describes a list of ACD agents. This structure can contain an array of LINEAGENTENTRY structures.
helpviewer_keywords: ["*LPLINEAGENTLIST","LINEAGENTLIST","LINEAGENTLIST structure [TAPI 2.2]","LPLINEAGENTLIST","LPLINEAGENTLIST structure pointer [TAPI 2.2]","_tapi2_lineagentlist","tapi/LINEAGENTLIST","tapi/LPLINEAGENTLIST","tapi2.lineagentlist"]
old-location: tapi2\lineagentlist.htm
tech.root: tapi3
ms.assetid: 176beb90-a9aa-4d40-9f84-e6ea9f84b5a2
ms.date: 12/05/2018
ms.keywords: '*LPLINEAGENTLIST, LINEAGENTLIST, LINEAGENTLIST structure [TAPI 2.2], LPLINEAGENTLIST, LPLINEAGENTLIST structure pointer [TAPI 2.2], _tapi2_lineagentlist, tapi/LINEAGENTLIST, tapi/LPLINEAGENTLIST, tapi2.lineagentlist'
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
req.typenames: LINEAGENTLIST, *LPLINEAGENTLIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineagentlist_tag
 - tapi/lineagentlist_tag
 - LPLINEAGENTLIST
 - tapi/LPLINEAGENTLIST
 - LINEAGENTLIST
 - tapi/LINEAGENTLIST
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
 - LINEAGENTLIST
---

# LINEAGENTLIST structure


## -description

The 
<b>LINEAGENTLIST</b> structure describes a list of ACD agents. This structure can contain an array of 
<a href="/windows/desktop/api/tapi/ns-tapi-lineagententry">LINEAGENTENTRY</a> structures.

## -struct-fields

### -field dwTotalSize

Total size allocated to this structure, in bytes.

### -field dwNeededSize

Size needed to hold all the information requested, in bytes.

### -field dwUsedSize

Size of the portion of this structure that contains useful information, in bytes.

### -field dwNumEntries

Number of 
<a href="/windows/desktop/api/tapi/ns-tapi-lineagententry">LINEAGENTENTRY</a> structures that appear in the list array. The value is zero if no agents are available.

### -field dwListSize

Size of the agent list array, in bytes.

### -field dwListOffset

Offset from the beginning of the structure to an array of 
<a href="/windows/desktop/api/tapi/ns-tapi-lineagententry">LINEAGENTENTRY</a> structures that specify information about agents. The <b>dwListOffset</b> member is <b>dwNumEntries</b> times SIZEOF(LINEAGENTENTRY). The size of the field is specified by <b>dwListSize</b>.

## -see-also

<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineagententry">LINEAGENTENTRY</a>