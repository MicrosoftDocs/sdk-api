---
UID: NS:routprot.IP_LOCAL_BINDING
title: IP_LOCAL_BINDING (routprot.h)
description: The IP_LOCAL_BINDING structure contains IP address information for an adapter.
helpviewer_keywords: ["*PIP_LOCAL_BINDING","IP_LOCAL_BINDING","IP_LOCAL_BINDING structure [RAS]","PIP_LOCAL_BINDING","PIP_LOCAL_BINDING structure pointer [RAS]","_mpr_ip_local_binding","routprot/IP_LOCAL_BINDING","routprot/PIP_LOCAL_BINDING","rras.ip_local_binding"]
old-location: rras\ip_local_binding.htm
tech.root: RRAS
ms.assetid: 121cc415-35eb-4c9b-a02d-c23be468d6bc
ms.date: 12/05/2018
ms.keywords: '*PIP_LOCAL_BINDING, IP_LOCAL_BINDING, IP_LOCAL_BINDING structure [RAS], PIP_LOCAL_BINDING, PIP_LOCAL_BINDING structure pointer [RAS], _mpr_ip_local_binding, routprot/IP_LOCAL_BINDING, routprot/PIP_LOCAL_BINDING, rras.ip_local_binding'
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
req.typenames: IP_LOCAL_BINDING, *PIP_LOCAL_BINDING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IP_LOCAL_BINDING
 - routprot/IP_LOCAL_BINDING
 - PIP_LOCAL_BINDING
 - routprot/PIP_LOCAL_BINDING
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
 - IP_LOCAL_BINDING
---

# IP_LOCAL_BINDING structure


## -description

The 
<b>IP_LOCAL_BINDING</b> structure contains IP address information for an adapter.

## -struct-fields

### -field Address

Specifies an IP address for the adapter.

### -field Mask

Specifies the subnet mask for the IP address.

## -remarks

Since an adapter can have more than one IP address, the 
<a href="/windows/desktop/api/routprot/ns-routprot-ip_adapter_binding_info">IP_ADAPTER_BINDING_INFO</a> structure maintains an array of 
<b>IP_LOCAL_BINDING</b> structures.

## -see-also

<a href="/windows/desktop/api/routprot/ns-routprot-ip_adapter_binding_info">IP_ADAPTER_BINDING_INFO</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>



<a href="/windows/desktop/RRAS/router-management-structures">Router Management Structures</a>