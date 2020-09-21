---
UID: NS:traffic._ENUMERATION_BUFFER
title: ENUMERATION_BUFFER (traffic.h)
description: The ENUMERATION_BUFFER structure contains information specific to a given flow, including flow name, the number of filters associated with the flow, and an array of filters associated with the flow.
helpviewer_keywords: ["*PENUMERATION_BUFFER","ENUMERATION_BUFFER","ENUMERATION_BUFFER structure [QOS]","PENUMERATION_BUFFER","PENUMERATION_BUFFER structure pointer [QOS]","_gqos_enumeration_buffer","qos.enumeration_buffer","traffic/ENUMERATION_BUFFER","traffic/PENUMERATION_BUFFER"]
old-location: qos\enumeration_buffer.htm
tech.root: QOS
ms.assetid: fd80b8c9-db0c-4e2c-b259-b21b06fc5d56
ms.date: 12/05/2018
ms.keywords: '*PENUMERATION_BUFFER, ENUMERATION_BUFFER, ENUMERATION_BUFFER structure [QOS], PENUMERATION_BUFFER, PENUMERATION_BUFFER structure pointer [QOS], _gqos_enumeration_buffer, qos.enumeration_buffer, traffic/ENUMERATION_BUFFER, traffic/PENUMERATION_BUFFER'
req.header: traffic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: ENUMERATION_BUFFER, *PENUMERATION_BUFFER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ENUMERATION_BUFFER
 - traffic/_ENUMERATION_BUFFER
 - PENUMERATION_BUFFER
 - traffic/PENUMERATION_BUFFER
 - ENUMERATION_BUFFER
 - traffic/ENUMERATION_BUFFER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Traffic.h
api_name:
 - ENUMERATION_BUFFER
---

# ENUMERATION_BUFFER structure


## -description

The 
<b>ENUMERATION_BUFFER</b> structure contains information specific to a given flow, including flow name, the number of filters associated with the flow, and an array of filters associated with the flow.

## -struct-fields

### -field Length

Number of bytes from the beginning of the 
<b>ENUMERATION_BUFFER</b> to the next 
<b>ENUMERATION_BUFFER</b>.

### -field OwnerProcessId

Identifies the owner of the process.

### -field FlowNameLength

Specifies the length of the <b>FlowName</b> member.

### -field FlowName

Array of WCHAR characters, of length <b>MAX_STRING_LENGTH</b>, that specifies the flow name.

### -field pFlow

Pointer to the corresponding 
<a href="/windows/desktop/api/traffic/ns-traffic-tc_gen_flow">TC_GEN_FLOW</a> structure. This structure is placed immediately after the array of TC_GEN_FILTERS and is included in <b>Length</b>.

### -field NumberOfFilters

Specifies the number of filters associated with the flow.

### -field GenericFilter

Array of 
<a href="/windows/desktop/api/traffic/ns-traffic-tc_gen_filter">TC_GEN_FILTER</a> structures. The number of elements in the array corresponds to the number of filters attached to the specified flow. Note that in order to enumerate through the array of 
<b>TC_GEN_FILTER</b> structures, you need to increment the pointer to the current 
<b>TC_GEN_FILTER</b> by using the following: 




sizeof(TC_GEN_FILTER) + 2 * [the pattern size of the current 
<a href="/windows/desktop/api/traffic/ns-traffic-tc_gen_filter">TC_GEN_FILTER</a> structure].

## -see-also

<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a>



<a href="/windows/desktop/api/traffic/ns-traffic-tc_gen_filter">TC_GEN_FILTER</a>



<a href="/windows/desktop/api/traffic/ns-traffic-tc_gen_flow">TC_GEN_FLOW</a>