---
UID: NS:lpmapi.Rsvp_Hop_IPv4
title: Rsvp_Hop_IPv4 (lpmapi.h)
description: The Rsvp_Hop_IPv4 structure stores information about an RSVP-enabled IPv4 hop.
helpviewer_keywords: ["Rsvp_Hop_IPv4","Rsvp_Hop_IPv4 structure [QOS]","lpmapi/Rsvp_Hop_IPv4","qos.rsvp_hop_ipv4"]
old-location: qos\rsvp_hop_ipv4.htm
tech.root: QOS
ms.assetid: 1a3f3e65-70f8-490c-8724-9e93c7fba457
ms.date: 12/05/2018
ms.keywords: Rsvp_Hop_IPv4, Rsvp_Hop_IPv4 structure [QOS], lpmapi/Rsvp_Hop_IPv4, qos.rsvp_hop_ipv4
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
req.typenames: Rsvp_Hop_IPv4
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Rsvp_Hop_IPv4
 - lpmapi/Rsvp_Hop_IPv4
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
 - Rsvp_Hop_IPv4
---

# Rsvp_Hop_IPv4 structure


## -description

The 
<b>Rsvp_Hop_IPv4</b> structure stores information about an RSVP-enabled IPv4 hop.

## -struct-fields

### -field hop_ipaddr

The next or previous hop IP address, in the form of an <a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">in_addr</a> structure.

### -field hop_LIH

Logical Interface Handle.

## -see-also

<a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">in_addr</a>

