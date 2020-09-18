---
UID: NS:traffic._TC_GEN_FILTER
title: TC_GEN_FILTER (traffic.h)
description: The TC_GEN_FILTER structure creates a filter that matches a certain set of packet attributes or criteria, which can subsequently be used to associate packets that meet the attribute criteria with a particular flow.
helpviewer_keywords: ["*PTC_GEN_FILTER","TC_GEN_FILTER","TC_GEN_FILTER structure [QOS]","TC_GEN_FILTER)","TC_GEN_FILTER) structure [QOS]","_gqos_tc_gen_filter","qos.tc_gen_filter","traffic/TC_GEN_FILTER"]
old-location: qos\tc_gen_filter.htm
tech.root: QOS
ms.assetid: 979bfa2d-50da-43a6-8ead-d338159e31cf
ms.date: 12/05/2018
ms.keywords: '*PTC_GEN_FILTER, TC_GEN_FILTER, TC_GEN_FILTER structure [QOS], TC_GEN_FILTER), TC_GEN_FILTER) structure [QOS], _gqos_tc_gen_filter, qos.tc_gen_filter, traffic/TC_GEN_FILTER'
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
req.typenames: TC_GEN_FILTER, *PTC_GEN_FILTER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TC_GEN_FILTER
 - traffic/_TC_GEN_FILTER
 - PTC_GEN_FILTER
 - traffic/PTC_GEN_FILTER
 - TC_GEN_FILTER
 - traffic/TC_GEN_FILTER
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
 - TC_GEN_FILTER)
---

# TC_GEN_FILTER structure


## -description

The 
<b>TC_GEN_FILTER</b> structure creates a filter that matches a certain set of packet attributes or criteria, which can subsequently be used to associate packets that meet the attribute criteria with a particular flow. The 
<b>TC_GEN_FILTER</b> structure uses its <b>AddressType</b> member to indicate a specific filter type to apply to the filter.

## -struct-fields

### -field AddressType

Defines the filter type to be applied with the filter, as defined in Ntddndis.h. With the designation of a specific filter in <b>AddressType</b>, the generic filter structure 
<b>TC_GEN_FILTER</b> provides a specific filter type.

### -field PatternSize

Size of the <b>Pattern</b> member, in bytes.

### -field Pattern

Indicates the specific format of the pattern to be applied to the filter, such as 
<a href="/windows/desktop/api/traffic/ns-traffic-ip_pattern">IP_PATTERN</a>. The pattern specifies which bits of a given packet should be evaluated when determining whether a packet is included in the filter.

### -field Mask

A bitmask applied to the bits designated in the <b>Pattern</b> member. The application of the <b>Mask</b> member to the <b>Pattern</b> member determines which bits in the <b>Pattern</b> member are significant (should be applied to the filter criteria). Note that the <b>Mask</b> member must be of the same type as the <b>Pattern</b> member.

## -see-also

<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a>



<a href="/windows/desktop/api/traffic/ns-traffic-ip_pattern">IP_PATTERN</a>