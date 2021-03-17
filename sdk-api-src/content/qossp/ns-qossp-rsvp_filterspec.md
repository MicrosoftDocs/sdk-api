---
UID: NS:qossp._RSVP_FILTERSPEC
title: RSVP_FILTERSPEC (qossp.h)
description: The RSVP_FILTERSPEC structure provides RSVP FILTERSPEC information.
helpviewer_keywords: ["*LPRSVP_FILTERSPEC","*LPRSVP_FILTERSPEC structure [QOS]","RSVP_FILTERSPEC","RSVP_FILTERSPEC structure [QOS]","qos.rsvp_filterspec","qossp/*LPRSVP_FILTERSPEC","qossp/RSVP_FILTERSPEC"]
old-location: qos\rsvp_filterspec.htm
tech.root: QOS
ms.assetid: ce4af25d-6c31-43a2-a30a-1d28b18e8f8b
ms.date: 12/05/2018
ms.keywords: '*LPRSVP_FILTERSPEC, *LPRSVP_FILTERSPEC structure [QOS], RSVP_FILTERSPEC, RSVP_FILTERSPEC structure [QOS], qos.rsvp_filterspec, qossp/*LPRSVP_FILTERSPEC, qossp/RSVP_FILTERSPEC'
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
req.typenames: RSVP_FILTERSPEC, *LPRSVP_FILTERSPEC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RSVP_FILTERSPEC
 - qossp/_RSVP_FILTERSPEC
 - LPRSVP_FILTERSPEC
 - qossp/LPRSVP_FILTERSPEC
 - RSVP_FILTERSPEC
 - qossp/RSVP_FILTERSPEC
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
 - RSVP_FILTERSPEC
---

# RSVP_FILTERSPEC structure


## -description

The <b>RSVP_FILTERSPEC</b> structure provides RSVP FILTERSPEC information.

## -struct-fields

### -field Type

Specifies the type of FILTERSPEC using the <b>FilterSpec</b> enumeration.

### -field FilterSpecV4

IPv4 FILTERSPEC information, provided in the form of a <a href="/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec_v4">RSVP_FILTERSPEC_V4</a> structure.

### -field FilterSpecV6

IPv6 FILTERSPEC information, provided in the form of a <a href="/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec_v6">RSVP_FILTERSPEC_V6</a> structure.

### -field FilterSpecV6Flow

IPv6 FILTERSPEC flow information, provided in the form of a <a href="/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec_v6_flow">RSVP_FILTERSPEC_V6_FLOW</a> structure.

### -field FilterSpecV4Gpi

IPv4 FILTERSPEC general port ID information, provided in the form of a <a href="/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec_v4_gpi">RSVP_FILTERSPEC_V4_GPI</a> structure.

### -field FilterSpecV6Gpi

IPv6 FILTERSPEC general port ID information, provided in the form of a <a href="/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec_v6_gpi">RSVP_FILTERSPEC_V6_GPI</a> structure.

## -see-also

<a href="/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec_v4">RSVP_FILTERSPEC_V4</a>



<a href="/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec_v4_gpi">RSVP_FILTERSPEC_V4_GPI</a>



<a href="/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec_v6">RSVP_FILTERSPEC_V6</a>



<a href="/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec_v6_flow">RSVP_FILTERSPEC_V6_FLOW</a>



<a href="/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec_v6_gpi">RSVP_FILTERSPEC_V6_GPI</a>