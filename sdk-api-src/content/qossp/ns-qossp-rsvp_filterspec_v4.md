---
UID: NS:qossp._RSVP_FILTERSPEC_V4
title: RSVP_FILTERSPEC_V4 (qossp.h)
description: The RSVP_FILTERSPEC_V4 structure stores information for a FILTERSPEC on an IPv4 address.
helpviewer_keywords: ["*LPRSVP_FILTERSPEC_V4","*LPRSVP_FILTERSPEC_V4 structure [QOS]","RSVP_FILTERSPEC_V4","RSVP_FILTERSPEC_V4 structure [QOS]","qos.rsvp_filterspec_v4","qossp/*LPRSVP_FILTERSPEC_V4","qossp/RSVP_FILTERSPEC_V4"]
old-location: qos\rsvp_filterspec_v4.htm
tech.root: QOS
ms.assetid: 038edc41-7324-4c5a-8172-c958cee05d5e
ms.date: 12/05/2018
ms.keywords: '*LPRSVP_FILTERSPEC_V4, *LPRSVP_FILTERSPEC_V4 structure [QOS], RSVP_FILTERSPEC_V4, RSVP_FILTERSPEC_V4 structure [QOS], qos.rsvp_filterspec_v4, qossp/*LPRSVP_FILTERSPEC_V4, qossp/RSVP_FILTERSPEC_V4'
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
req.typenames: RSVP_FILTERSPEC_V4, *LPRSVP_FILTERSPEC_V4
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RSVP_FILTERSPEC_V4
 - qossp/_RSVP_FILTERSPEC_V4
 - LPRSVP_FILTERSPEC_V4
 - qossp/LPRSVP_FILTERSPEC_V4
 - RSVP_FILTERSPEC_V4
 - qossp/RSVP_FILTERSPEC_V4
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
 - RSVP_FILTERSPEC_V4
---

# RSVP_FILTERSPEC_V4 structure


## -description

The <b>RSVP_FILTERSPEC_V4</b> structure stores information for a FILTERSPEC on an IPv4 address.

## -struct-fields

### -field Address

IPv4 address for which the FILTERSPEC applies, expressed as an <a href="/windows/desktop/api/qossp/ns-qossp-in_addr_ipv4">IN_ADDR_IPV4</a> union.

### -field Unused

Reserved. Set to zero.

### -field Port

TCP port of the socket on which the FILTERSPEC applies.

## -remarks

When working with IPv6 addresses, use <a href="/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec_v6">RSVP_FILTERSPEC_V6</a>.

## -see-also

<a href="/windows/desktop/api/qossp/ns-qossp-in_addr_ipv4">IN_ADDR_IPV4</a>



<a href="/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec_v6">RSVP_FILTERSPEC_V6</a>