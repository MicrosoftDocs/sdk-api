---
UID: NE:qossp.__unnamed_enum_0
title: FilterType (qossp.h)
description: The FilterType enumeration specifies the type of filter used for an RSVP FILTERSPEC.
helpviewer_keywords: ["FILTERSPECV4","FILTERSPECV4_GPI","FILTERSPECV6","FILTERSPECV6_FLOW","FILTERSPECV6_GPI","FILTERSPEC_END","FilterType","FilterType enumeration [QOS]","qos.filtertype","qossp/FILTERSPECV4","qossp/FILTERSPECV4_GPI","qossp/FILTERSPECV6","qossp/FILTERSPECV6_FLOW","qossp/FILTERSPECV6_GPI","qossp/FILTERSPEC_END","qossp/FilterType"]
old-location: qos\filtertype.htm
tech.root: QOS
ms.assetid: e9e961ed-80a8-4694-a11d-f6cd323ec2ff
ms.date: 12/05/2018
ms.keywords: FILTERSPECV4, FILTERSPECV4_GPI, FILTERSPECV6, FILTERSPECV6_FLOW, FILTERSPECV6_GPI, FILTERSPEC_END, FilterType, FilterType enumeration [QOS], qos.filtertype, qossp/FILTERSPECV4, qossp/FILTERSPECV4_GPI, qossp/FILTERSPECV6, qossp/FILTERSPECV6_FLOW, qossp/FILTERSPECV6_GPI, qossp/FILTERSPEC_END, qossp/FilterType
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
req.typenames: FilterType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FilterType
 - qossp/FilterType
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
 - FilterType
---

# FilterType enumeration


## -description

The <b>FilterType</b> enumeration specifies the type of filter used for an RSVP FILTERSPEC.

## -enum-fields

### -field FILTERSPECV4:1

Indicates an IPv4 FILTERSPEC.

### -field FILTERSPECV6

Indicates an IPv6 FILTERSPEC.

### -field FILTERSPECV6_FLOW

Indicates  IPv6 FILTERSPEC flow information.

### -field FILTERSPECV4_GPI

Indicates  IPv4 FILTERSPEC general port identifier information.

### -field FILTERSPECV6_GPI

Indicates  IPv6 FILTERSPEC general port identifier information.

### -field FILTERSPEC_END

Indicates  the end of the FILTERSPEC information.

## -see-also

<a href="/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec_v4">RSVP_FILTERSPEC_V4</a>



<a href="/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec_v4_gpi">RSVP_FILTERSPEC_V4_GPI</a>



<a href="/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec_v6">RSVP_FILTERSPEC_V6</a>



<a href="/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec_v6_flow">RSVP_FILTERSPEC_V6_FLOW</a>



<a href="/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec_v6_gpi">RSVP_FILTERSPEC_V6_GPI</a>
