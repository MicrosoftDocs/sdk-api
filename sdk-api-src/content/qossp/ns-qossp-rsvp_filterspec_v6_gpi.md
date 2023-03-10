---
UID: NS:qossp._RSVP_FILTERSPEC_V6_GPI
title: RSVP_FILTERSPEC_V6_GPI (qossp.h)
description: The RSVP_FILTERSPEC_V6_GPI structure provides general port identifier information for a given FILTERSPEC on an IPv6 address.
helpviewer_keywords: ["*LPRSVP_FILTERSPEC_V6_GPI","*LPRSVP_FILTERSPEC_V6_GPI structure [QOS]","RSVP_FILTERSPEC_V6_GPI","RSVP_FILTERSPEC_V6_GPI structure [QOS]","qos.rsvp_filterspec_v6_gpi","qossp/*LPRSVP_FILTERSPEC_V6_GPI","qossp/RSVP_FILTERSPEC_V6_GPI"]
old-location: qos\rsvp_filterspec_v6_gpi.htm
tech.root: QOS
ms.assetid: ede040f4-4858-42d8-a4b5-af6e79c036d7
ms.date: 12/05/2018
ms.keywords: '*LPRSVP_FILTERSPEC_V6_GPI, *LPRSVP_FILTERSPEC_V6_GPI structure [QOS], RSVP_FILTERSPEC_V6_GPI, RSVP_FILTERSPEC_V6_GPI structure [QOS], qos.rsvp_filterspec_v6_gpi, qossp/*LPRSVP_FILTERSPEC_V6_GPI, qossp/RSVP_FILTERSPEC_V6_GPI'
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
req.typenames: RSVP_FILTERSPEC_V6_GPI, *LPRSVP_FILTERSPEC_V6_GPI
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RSVP_FILTERSPEC_V6_GPI
 - qossp/_RSVP_FILTERSPEC_V6_GPI
 - LPRSVP_FILTERSPEC_V6_GPI
 - qossp/LPRSVP_FILTERSPEC_V6_GPI
 - RSVP_FILTERSPEC_V6_GPI
 - qossp/RSVP_FILTERSPEC_V6_GPI
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
 - RSVP_FILTERSPEC_V6_GPI
---

# RSVP_FILTERSPEC_V6_GPI structure


## -description

The <b>RSVP_FILTERSPEC_V6_GPI</b> structure provides general port identifier information for a given FILTERSPEC on an IPv6 address.

## -struct-fields

### -field Address

IPv4 address for which the FILTERSPEC general port identifier applies, expressed as an <a href="/windows/desktop/api/qossp/ns-qossp-in_addr_ipv6">IN_ADDR_IPV6</a> structure.

### -field GeneralPortId

General Port Identifier for the FILTERSPEC.

## -remarks

When working with IPv4 addresses, use <a href="/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec_v4_gpi">RSVP_FILTERSPEC_V4_GPI</a>.

## -see-also

<a href="/windows/desktop/api/qossp/ns-qossp-in_addr_ipv6">IN_ADDR_IPV6</a>



<a href="/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec_v4_gpi">RSVP_FILTERSPEC_V4_GPI</a>