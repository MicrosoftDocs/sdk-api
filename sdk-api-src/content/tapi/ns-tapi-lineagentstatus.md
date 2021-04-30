---
UID: NS:tapi.lineagentstatus_tag
title: LINEAGENTSTATUS (tapi.h)
description: The LINEAGENTSTATUS structure describes the current status of an ACD agent. The lineGetAgentStatus function returns the LINEAGENTSTATUS structure.
helpviewer_keywords: ["*LPLINEAGENTSTATUS","LINEAGENTSTATUS","LINEAGENTSTATUS structure [TAPI 2.2]","LPLINEAGENTSTATUS","LPLINEAGENTSTATUS structure pointer [TAPI 2.2]","_tapi2_lineagentstatus_str","tapi/LINEAGENTSTATUS","tapi/LPLINEAGENTSTATUS","tapi2.lineagentstatus_str"]
old-location: tapi2\lineagentstatus_str.htm
tech.root: tapi3
ms.assetid: c846bd16-79d2-4af0-b3ad-7432c28c542b
ms.date: 12/05/2018
ms.keywords: '*LPLINEAGENTSTATUS, LINEAGENTSTATUS, LINEAGENTSTATUS structure [TAPI 2.2], LPLINEAGENTSTATUS, LPLINEAGENTSTATUS structure pointer [TAPI 2.2], _tapi2_lineagentstatus_str, tapi/LINEAGENTSTATUS, tapi/LPLINEAGENTSTATUS, tapi2.lineagentstatus_str'
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
req.typenames: LINEAGENTSTATUS, *LPLINEAGENTSTATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineagentstatus_tag
 - tapi/lineagentstatus_tag
 - LPLINEAGENTSTATUS
 - tapi/LPLINEAGENTSTATUS
 - LINEAGENTSTATUS
 - tapi/LINEAGENTSTATUS
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
 - LINEAGENTSTATUS
---

# LINEAGENTSTATUS structure


## -description

The 
<b>LINEAGENTSTATUS</b> structure describes the current status of an ACD agent. The 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetagentstatusa">lineGetAgentStatus</a> function returns the 
<b>LINEAGENTSTATUS</b> structure.

## -struct-fields

### -field dwTotalSize

Total size allocated to this data structure, in bytes.

### -field dwNeededSize

Size needed to hold all the information requested, in bytes.

### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.

### -field dwNumEntries

Number of 
<a href="/windows/desktop/api/tapi/ns-tapi-lineagentgroupentry">LINEAGENTGROUPENTRY</a> structures that appear in the <i>GroupList</i> array. The value is 0 if no agent is logged in on the address.

### -field dwGroupListSize

Size of the group list array, in bytes.

### -field dwGroupListOffset

Offset from the beginning of this structure to an array of 
<a href="/windows/desktop/api/tapi/ns-tapi-lineagentgroupentry">LINEAGENTGROUPENTRY</a> structures. The size is <b>dwNumEntries</b> times SIZEOF(LINEAGENTGROUPENTRY). The array contains groups into which the agent is currently logged in on the address. The size of the field is specified by <b>dwGroupListSize</b>.

### -field dwState

Current state of the agent. One of the 
<a href="/windows/desktop/Tapi/lineagentstate--constants">LINEAGENTSTATE_ constants</a>.

### -field dwNextState

State into which the agent is automatically placed when the current call completes. One of the <a href="/windows/desktop/Tapi/lineagentstate--constants">LINEAGENTSTATE_ constants</a>.

### -field dwActivityID

Identifier of the current agent activity.

### -field dwActivitySize

Size of the agent activity string, in bytes.

### -field dwActivityOffset

Offset from the beginning of the structure to a null-terminated string specifying the current agent activity. The size of the string is specified by <b>dwActivitySize</b>.

### -field dwAgentFeatures

Agent-related features available at the time the status was obtained, using the 
<a href="/windows/desktop/Tapi/lineagentfeature--constants">LINEAGENTFEATURE_ constants</a>.

### -field dwValidStates

Agent states that could be selected, at this point in time, using 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetagentstate">lineSetAgentState</a>. Consists of one or more of the 
<a href="/windows/desktop/Tapi/lineagentstate--constants">LINEAGENTSTATE_ constants</a>.

### -field dwValidNextStates

Next agent states that could be selected, at this point in time, by calling the 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetagentstate">lineSetAgentState</a> function. Consists of one or more of the <a href="/windows/desktop/Tapi/lineagentstate--constants">LINEAGENTSTATE_ constants</a>.

## -see-also

<a href="/windows/desktop/Tapi/lineagentfeature--constants">LINEAGENTFEATURE_ constants</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineagentgroupentry">LINEAGENTGROUPENTRY</a>



<a href="/windows/desktop/Tapi/lineagentstate--constants">LINEAGENTSTATE_ constants</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetagentstatusa">lineGetAgentStatus</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetagentstate">lineSetAgentState</a>