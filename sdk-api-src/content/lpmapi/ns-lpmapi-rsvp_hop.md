---
UID: NS:lpmapi.RSVP_HOP
title: RSVP_HOP (lpmapi.h)
description: The RSVP_HOP structure contains information about an RSVP-enabled hop.
helpviewer_keywords: ["RSVP_HOP","RSVP_HOP structure [QOS]","lpmapi/RSVP_HOP","qos.rsvp_hop"]
old-location: qos\rsvp_hop.htm
tech.root: QOS
ms.assetid: 4b23bc0e-ccea-4161-93fa-b136099e88bd
ms.date: 12/05/2018
ms.keywords: RSVP_HOP, RSVP_HOP structure [QOS], lpmapi/RSVP_HOP, qos.rsvp_hop
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
req.typenames: RSVP_HOP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RSVP_HOP
 - lpmapi/RSVP_HOP
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
 - RSVP_HOP
---

# RSVP_HOP structure


## -description

The 
<b>RSVP_HOP</b> structure contains information about an RSVP-enabled hop.

## -struct-fields

### -field hop_header

RSVP hop header, in the form of an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvpobjhdr">RsvpObjHdr</a> structure

### -field hop_u

#### hop_ipv4

Information about the IPv4 hop, in the form of an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvp_hop_ipv4">Rsvp_Hop_IPv4</a> structure.

### -field hop_ipv4

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvpobjhdr">RsvpObjHdr</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvp_hop_ipv4">Rsvp_Hop_IPv4</a>

