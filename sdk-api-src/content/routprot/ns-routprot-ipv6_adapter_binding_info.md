---
UID: NS:routprot.IPV6_ADAPTER_BINDING_INFO
title: IPV6_ADAPTER_BINDING_INFO (routprot.h)
description: The IPV6_ADAPTER_BINDING_INFO structure contains IPv6-specific information for a particular network adapter.
helpviewer_keywords: ["*PIPV6_ADAPTER_BINDING_INFO","IPV6_ADAPTER_BINDING_INFO","IPV6_ADAPTER_BINDING_INFO structure [RAS]","PIPV6_ADAPTER_BINDING_INFO","PIPV6_ADAPTER_BINDING_INFO structure pointer [RAS]","routprot/IPV6_ADAPTER_BINDING_INFO","routprot/PIPV6_ADAPTER_BINDING_INFO","rras.ipv6_adapter_binding_info"]
old-location: rras\ipv6_adapter_binding_info.htm
tech.root: RRAS
ms.assetid: 1e964f09-96c6-432b-bb1a-026a3ea0deba
ms.date: 12/05/2018
ms.keywords: '*PIPV6_ADAPTER_BINDING_INFO, IPV6_ADAPTER_BINDING_INFO, IPV6_ADAPTER_BINDING_INFO structure [RAS], PIPV6_ADAPTER_BINDING_INFO, PIPV6_ADAPTER_BINDING_INFO structure pointer [RAS], routprot/IPV6_ADAPTER_BINDING_INFO, routprot/PIPV6_ADAPTER_BINDING_INFO, rras.ipv6_adapter_binding_info'
req.header: routprot.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: IPV6_ADAPTER_BINDING_INFO, *PIPV6_ADAPTER_BINDING_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPV6_ADAPTER_BINDING_INFO
 - routprot/IPV6_ADAPTER_BINDING_INFO
 - PIPV6_ADAPTER_BINDING_INFO
 - routprot/PIPV6_ADAPTER_BINDING_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Routprot.h
api_name:
 - IPV6_ADAPTER_BINDING_INFO
---

# IPV6_ADAPTER_BINDING_INFO structure


## -description

The 
<b>IPV6_ADAPTER_BINDING_INFO</b> structure contains IPv6-specific information for a particular network adapter.

## -struct-fields

### -field AddressCount

The number of IPv6 addresses associated with this adapter.

### -field RemoteAddress

This member is for WAN interfaces. An <a href="/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)">in6_addr</a> structure that contains the address of the machine at the other end of a dial-up link.

### -field Mtu

Reserved for future use.

### -field Speed

Reserved for future use.

### -field Address

Pointer to an array of 
<a href="/windows/desktop/api/routprot/ns-routprot-ipv6_local_binding">IPV6_LOCAL_BINDING</a> structures. The array  contains a structure for each of the IPv6 addresses associated with this adapter.

## -remarks

Since an adapter can have more than one IP address, the 
<b>IPV6_ADAPTER_BINDING_INFO</b> structure maintains an array of 
<a href="/windows/desktop/api/routprot/ns-routprot-ipv6_local_binding">IPV6_LOCAL_BINDING</a> structures.

## -see-also

<a href="/windows/desktop/api/routprot/ns-routprot-ipv6_local_binding">IPV6_LOCAL_BINDING</a>



<a href="/windows/desktop/api/routprot/ns-routprot-ip_adapter_binding_info">IP_ADAPTER_BINDING_INFO</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>



<a href="/windows/desktop/RRAS/router-management-structures">Router Management Structures</a>