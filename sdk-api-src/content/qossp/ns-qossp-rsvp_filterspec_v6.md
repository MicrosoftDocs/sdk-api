---
UID: NS:qossp._RSVP_FILTERSPEC_V6
title: RSVP_FILTERSPEC_V6 (qossp.h)
description: The RSVP_FILTERSPEC_V6 structure stores information for a FILTERSPEC on an IPv6 address.
helpviewer_keywords: ["*LPRSVP_FILTERSPEC_V6","RSVP_FILTERSPEC_V6","RSVP_FILTERSPEC_V6 structure [QOS]","qos.rsvp_filterspec_v6","qossp/RSVP_FILTERSPEC_V6"]
old-location: qos\rsvp_filterspec_v6.htm
tech.root: QOS
ms.assetid: 7e567714-1d91-4dd4-a560-2b57876c837c
ms.date: 12/05/2018
ms.keywords: '*LPRSVP_FILTERSPEC_V6, RSVP_FILTERSPEC_V6, RSVP_FILTERSPEC_V6 structure [QOS], qos.rsvp_filterspec_v6, qossp/RSVP_FILTERSPEC_V6'
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
req.typenames: RSVP_FILTERSPEC_V6, *LPRSVP_FILTERSPEC_V6
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RSVP_FILTERSPEC_V6
 - qossp/_RSVP_FILTERSPEC_V6
 - LPRSVP_FILTERSPEC_V6
 - qossp/LPRSVP_FILTERSPEC_V6
 - RSVP_FILTERSPEC_V6
 - qossp/RSVP_FILTERSPEC_V6
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
 - RSVP_FILTERSPEC_V6
---

# RSVP_FILTERSPEC_V6 structure


## -description

The <b>RSVP_FILTERSPEC_V6</b> structure  stores information for a FILTERSPEC on an IPv6 address.

## -struct-fields

### -field Address

IPv4 address for which the FILTERSPEC applies, expressed as an <a href="/windows/desktop/api/qossp/ns-qossp-in_addr_ipv6">IN_ADDR_IPV6</a> structure.

### -field UnUsed

### -field Port

TCP port of the socket on which the FILTERSPEC applies.

### -field Unused

Reserved. Set to zero.

## -remarks

When working with IPv4 addresses, use <a href="/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec_v4">RSVP_FILTERSPEC_V4</a>.

## -see-also

<a href="/windows/desktop/api/qossp/ns-qossp-in_addr_ipv6">IN_ADDR_IPV6</a>



<a href="/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec_v4">RSVP_FILTERSPEC_V4</a>