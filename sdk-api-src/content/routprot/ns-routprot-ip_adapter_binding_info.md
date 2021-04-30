---
UID: NS:routprot.IP_ADAPTER_BINDING_INFO
title: IP_ADAPTER_BINDING_INFO (routprot.h)
description: The IP_ADAPTER_BINDING_INFO structure contains IP-specific information for a particular network adapter.
helpviewer_keywords: ["*PIP_ADAPTER_BINDING_INFO","IP_ADAPTER_BINDING_INFO","IP_ADAPTER_BINDING_INFO structure [RAS]","PIP_ADAPTER_BINDING_INFO","PIP_ADAPTER_BINDING_INFO structure pointer [RAS]","_mpr_ip_adapter_binding_info","routprot/IP_ADAPTER_BINDING_INFO","routprot/PIP_ADAPTER_BINDING_INFO","rras.ip_adapter_binding_info"]
old-location: rras\ip_adapter_binding_info.htm
tech.root: RRAS
ms.assetid: 3eb864e7-2de6-44c2-af3e-fee547de6081
ms.date: 12/05/2018
ms.keywords: '*PIP_ADAPTER_BINDING_INFO, IP_ADAPTER_BINDING_INFO, IP_ADAPTER_BINDING_INFO structure [RAS], PIP_ADAPTER_BINDING_INFO, PIP_ADAPTER_BINDING_INFO structure pointer [RAS], _mpr_ip_adapter_binding_info, routprot/IP_ADAPTER_BINDING_INFO, routprot/PIP_ADAPTER_BINDING_INFO, rras.ip_adapter_binding_info'
req.header: routprot.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: IP_ADAPTER_BINDING_INFO, *PIP_ADAPTER_BINDING_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IP_ADAPTER_BINDING_INFO
 - routprot/IP_ADAPTER_BINDING_INFO
 - PIP_ADAPTER_BINDING_INFO
 - routprot/PIP_ADAPTER_BINDING_INFO
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
 - IP_ADAPTER_BINDING_INFO
---

# IP_ADAPTER_BINDING_INFO structure


## -description

The 
<b>IP_ADAPTER_BINDING_INFO</b> structure contains IP-specific information for a particular network adapter.

## -struct-fields

### -field AddressCount

The number of IP addresses associated with this adapter.

### -field RemoteAddress

This member is for WAN interfaces. It contains the address of the machine at the other end of a dial-up link.

### -field Mtu

Reserved for future use.

### -field Speed

Reserved for future use.

### -field Address

Pointer to an array of 
<a href="/windows/desktop/api/routprot/ns-routprot-ip_local_binding">IP_LOCAL_BINDING</a> structures. The array  contains a structure for each of the IP addresses associated with this adapter.

## -remarks

Since an adapter can have more than one IP address, the 
<b>IP_ADAPTER_BINDING_INFO</b> structure maintains an array of 
<a href="/windows/desktop/api/routprot/ns-routprot-ip_local_binding">IP_LOCAL_BINDING</a> structures.

## -see-also

<a href="/windows/desktop/api/routprot/ns-routprot-ip_local_binding">IP_LOCAL_BINDING</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>



<a href="/windows/desktop/RRAS/router-management-structures">Router Management Structures</a>