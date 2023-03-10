---
UID: NS:qossp._RSVP_FILTERSPEC_V6_FLOW
title: RSVP_FILTERSPEC_V6_FLOW (qossp.h)
description: The RSVP_FILTERSPEC_V6_FLOW structure provides flow label information for an IPv6 FILTERSPEC.
helpviewer_keywords: ["*LPRSVP_FILTERSPEC_V6_FLOW","*LPRSVP_FILTERSPEC_V6_FLOW structure [QOS]","RSVP_FILTERSPEC_V6_FLOW","RSVP_FILTERSPEC_V6_FLOW structure [QOS]","qos.rsvp_filterspec_v6_flow","qossp/*LPRSVP_FILTERSPEC_V6_FLOW","qossp/RSVP_FILTERSPEC_V6_FLOW"]
old-location: qos\rsvp_filterspec_v6_flow.htm
tech.root: QOS
ms.assetid: 5bca12be-5bc4-40b2-bc72-52cf0297821b
ms.date: 12/05/2018
ms.keywords: '*LPRSVP_FILTERSPEC_V6_FLOW, *LPRSVP_FILTERSPEC_V6_FLOW structure [QOS], RSVP_FILTERSPEC_V6_FLOW, RSVP_FILTERSPEC_V6_FLOW structure [QOS], qos.rsvp_filterspec_v6_flow, qossp/*LPRSVP_FILTERSPEC_V6_FLOW, qossp/RSVP_FILTERSPEC_V6_FLOW'
req.header: qossp.h
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
req.typenames: RSVP_FILTERSPEC_V6_FLOW, *LPRSVP_FILTERSPEC_V6_FLOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RSVP_FILTERSPEC_V6_FLOW
 - qossp/_RSVP_FILTERSPEC_V6_FLOW
 - LPRSVP_FILTERSPEC_V6_FLOW
 - qossp/LPRSVP_FILTERSPEC_V6_FLOW
 - RSVP_FILTERSPEC_V6_FLOW
 - qossp/RSVP_FILTERSPEC_V6_FLOW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Qossp.h
api_name:
 - RSVP_FILTERSPEC_V6_FLOW
---

# RSVP_FILTERSPEC_V6_FLOW structure


## -description

The <b>RSVP_FILTERSPEC_V6_FLOW</b> structure provides flow label information for an IPv6 FILTERSPEC.

## -struct-fields

### -field Address

IPv4 address for which the FILTERSPEC flow label applies, expressed as an <a href="/windows/desktop/api/qossp/ns-qossp-in_addr_ipv6">IN_ADDR_IPV6</a> structure.

### -field UnUsed

### -field FlowLabel

Label for the flow.

### -field Unused

Reserved. Do not use.

## -see-also

<a href="/windows/desktop/api/qossp/ns-qossp-in_addr_ipv6">IN_ADDR_IPV6</a>



<a href="/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec_v6">RSVP_FILTERSPEC_V6</a>