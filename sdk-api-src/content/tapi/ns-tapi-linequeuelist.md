---
UID: NS:tapi.linequeuelist_tag
title: LINEQUEUELIST (tapi.h)
description: The LINEQUEUELIST structure describes a list of queues. This structure can contain an array of LINEQUEUEENTRY structures. The lineGetQueueList function returns the LINEQUEUELIST structure. LINEQUEUELIST requires TAPI 3.0 version negotiation.
helpviewer_keywords: ["*LPLINEQUEUELIST","LINEQUEUELIST","LINEQUEUELIST structure [TAPI 2.2]","LPLINEQUEUELIST","LPLINEQUEUELIST structure pointer [TAPI 2.2]","_tapi2_linequeuelist","tapi/LINEQUEUELIST","tapi/LPLINEQUEUELIST","tapi2.linequeuelist"]
old-location: tapi2\linequeuelist.htm
tech.root: tapi3
ms.assetid: 86645d7c-f683-48e7-8342-3e9d5961913a
ms.date: 12/05/2018
ms.keywords: '*LPLINEQUEUELIST, LINEQUEUELIST, LINEQUEUELIST structure [TAPI 2.2], LPLINEQUEUELIST, LPLINEQUEUELIST structure pointer [TAPI 2.2], _tapi2_linequeuelist, tapi/LINEQUEUELIST, tapi/LPLINEQUEUELIST, tapi2.linequeuelist'
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
req.typenames: LINEQUEUELIST, *LPLINEQUEUELIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - linequeuelist_tag
 - tapi/linequeuelist_tag
 - LPLINEQUEUELIST
 - tapi/LPLINEQUEUELIST
 - LINEQUEUELIST
 - tapi/LINEQUEUELIST
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
 - LINEQUEUELIST
---

# LINEQUEUELIST structure


## -description

The 
<b>LINEQUEUELIST</b> structure describes a list of queues. This structure can contain an array of 
<a href="/windows/desktop/api/tapi/ns-tapi-linequeueentry">LINEQUEUEENTRY</a> structures. The 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetqueuelista">lineGetQueueList</a> function returns the 
<b>LINEQUEUELIST</b> structure. 
<b>LINEQUEUELIST</b> requires TAPI 3.0 version negotiation.

## -struct-fields

### -field dwTotalSize

Total size allocated to this structure, in bytes.

### -field dwNeededSize

Size needed to hold all the information requested, in bytes.

### -field dwUsedSize

Size of the portion of this structure that contains useful information, in bytes.

### -field dwNumEntries

Number of 
<a href="/windows/desktop/api/tapi/ns-tapi-linequeueentry">LINEQUEUEENTRY</a> structures that appear in the list array. The value is zero if no queue is available.

### -field dwListSize

Size of the agent information array, in bytes.

### -field dwListOffset

Offset from the beginning of the structure to an array of 
<a href="/windows/desktop/api/tapi/ns-tapi-linequeueentry">LINEQUEUEENTRY</a> structure that specify information about agents. The <b>dwListOffset</b> member is <b>dwNumEntries</b> times SIZEOF(LINEQUEUEENTRY). The size of the field is specified by <b>dwListSize</b>.

## -see-also

<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linequeueentry">LINEQUEUEENTRY</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetqueuelista">lineGetQueueList</a>