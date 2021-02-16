---
UID: NS:routprot.IPV6_LOCAL_BINDING
title: IPV6_LOCAL_BINDING (routprot.h)
description: The IPV6_LOCAL_BINDING structure contains IPv6 address information for an adapter.
helpviewer_keywords: ["*PIPV6_LOCAL_BINDING","IPV6_LOCAL_BINDING","IPV6_LOCAL_BINDING structure [RAS]","PIPV6_LOCAL_BINDING","PIPV6_LOCAL_BINDING structure pointer [RAS]","routprot/IPV6_LOCAL_BINDING","routprot/PIPV6_LOCAL_BINDING","rras.ipv6_local_binding"]
old-location: rras\ipv6_local_binding.htm
tech.root: RRAS
ms.assetid: c698fa3b-04d5-4401-9ab3-a200211cff24
ms.date: 12/05/2018
ms.keywords: '*PIPV6_LOCAL_BINDING, IPV6_LOCAL_BINDING, IPV6_LOCAL_BINDING structure [RAS], PIPV6_LOCAL_BINDING, PIPV6_LOCAL_BINDING structure pointer [RAS], routprot/IPV6_LOCAL_BINDING, routprot/PIPV6_LOCAL_BINDING, rras.ipv6_local_binding'
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
req.typenames: IPV6_LOCAL_BINDING, *PIPV6_LOCAL_BINDING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPV6_LOCAL_BINDING
 - routprot/IPV6_LOCAL_BINDING
 - PIPV6_LOCAL_BINDING
 - routprot/PIPV6_LOCAL_BINDING
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
 - IPV6_LOCAL_BINDING
---

# IPV6_LOCAL_BINDING structure


## -description

The 
<b>IPV6_LOCAL_BINDING</b> structure contains IPv6 address information for an adapter.

## -struct-fields

### -field Address

An <a href="/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)">in6_addr</a> structure that specifies an IPv6 address for the adapter.

### -field PrefixLength

The length, in bits, of the address prefix.

## -remarks

Since an adapter can have more than one IP address, the 
<a href="/windows/desktop/api/routprot/ns-routprot-ipv6_adapter_binding_info">IPV6_ADAPTER_BINDING_INFO</a> structure maintains an array of 
<b>IPV6_LOCAL_BINDING</b> structures.

## -see-also

<a href="/windows/desktop/api/routprot/ns-routprot-ipv6_adapter_binding_info">IPV6_ADAPTER_BINDING_INFO</a>



<a href="/windows/desktop/api/routprot/ns-routprot-ip_local_binding">IP_LOCAL_BINDING</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>



<a href="/windows/desktop/RRAS/router-management-structures">Router Management Structures</a>