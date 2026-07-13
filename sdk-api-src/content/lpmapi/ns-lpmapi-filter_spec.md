---
UID: NS:lpmapi.FILTER_SPEC
title: FILTER_SPEC (lpmapi.h)
description: The FILTER_SPEC structure stores information about an RSVP FILTERSPEC.
helpviewer_keywords: ["FILTER_SPEC","FILTER_SPEC structure [QOS]","SENDER_TEMPLATE","lpmapi/FILTER_SPEC","qos.filter_spec"]
old-location: qos\filter_spec.htm
tech.root: QOS
ms.assetid: 72d08944-7ac9-496f-a18b-e6fcddb59c56
ms.date: 12/05/2018
ms.keywords: FILTER_SPEC, FILTER_SPEC structure [QOS], SENDER_TEMPLATE, lpmapi/FILTER_SPEC, qos.filter_spec
req.header: lpmapi.h
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
req.typenames: FILTER_SPEC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FILTER_SPEC
 - lpmapi/FILTER_SPEC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lpmapi.h
api_name:
 - FILTER_SPEC
---

# FILTER_SPEC structure


## -description

The 
<b>FILTER_SPEC</b> structure stores information about an RSVP FILTERSPEC.

## -struct-fields

### -field filt_header

RSVP Object Header for the FILTERSPEC, in the form of an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvpobjhdr">RsvpObjHdr</a> structure.

### -field filt_u

#### filt_ipv4

FILTERSPEC, in the form of a <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-filter_spec_ipv4">Filter_Spec_IPv4</a> header.



#### filt_ipv4gpi

FILTERSPEC GPI information, in the form of a <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-filter_spec_ipv4gpi">Filter_Spec_IPv4GPI</a> header.

### -field filt_ipv4

### -field filt_ipv4gpi

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-filter_spec_ipv4">Filter_Spec_IPv4</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-filter_spec_ipv4gpi">Filter_Spec_IPv4GPI</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvpobjhdr">RsvpObjHdr</a>

