---
UID: NS:fwpmtypes.FWPM_NET_EVENT_CAPABILITY_ALLOW0_
title: FWPM_NET_EVENT_CAPABILITY_ALLOW0 (fwpmtypes.h)
description: Contains information about network traffic allowed in relation to an app container network capability.
helpviewer_keywords: ["FWPM_NET_EVENT_CAPABILITY_ALLOW0","FWPM_NET_EVENT_CAPABILITY_ALLOW0 structure [Filtering]","fwp.fwpm_net_event_capability_allow0","fwpmtypes/FWPM_NET_EVENT_CAPABILITY_ALLOW0"]
old-location: fwp\fwpm_net_event_capability_allow0.htm
tech.root: fwp
ms.assetid: e53e92e5-f7fa-4457-8681-754b50b24273
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_CAPABILITY_ALLOW0, FWPM_NET_EVENT_CAPABILITY_ALLOW0 structure [Filtering], fwp.fwpm_net_event_capability_allow0, fwpmtypes/FWPM_NET_EVENT_CAPABILITY_ALLOW0
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWPM_NET_EVENT_CAPABILITY_ALLOW0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_NET_EVENT_CAPABILITY_ALLOW0_
 - fwpmtypes/FWPM_NET_EVENT_CAPABILITY_ALLOW0_
 - FWPM_NET_EVENT_CAPABILITY_ALLOW0
 - fwpmtypes/FWPM_NET_EVENT_CAPABILITY_ALLOW0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_NET_EVENT_CAPABILITY_ALLOW0
---

# FWPM_NET_EVENT_CAPABILITY_ALLOW0 structure


## -description

The <b>FWPM_NET_EVENT_CAPABILITY_ALLOW0</b> structure contains information about network traffic allowed in relation to an app container network capability.. The specified app container network capability grants access to network resources, and  the specified filter identifier enforces allowing access.

## -struct-fields

### -field networkCapabilityId

Type: <b><a href="/windows/win32/api/fwpmtypes/ne-fwpmtypes-fwpm_appc_network_capability_type">FWPM_APPC_NETWORK_CAPABILITY_TYPE</a></b>

The specific app container network capability allowing this traffic.

### -field filterId

Type: <b>UINT64</b>

A LUID identifying the WFP filter enforcing the allowed access intended by the capability in <b>networkCapabilityId</b>.

### -field isLoopback

Type: <b>BOOL</b>

True if the packet originated from (or was heading to) the loopback adapter; otherwise, false.

## -see-also

<a href="/windows/win32/api/fwpmtypes/ne-fwpmtypes-fwpm_appc_network_capability_type">FWPM_APPC_NETWORK_CAPABILITY_TYPE</a>



<a href="/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_drop0">FWPM_NET_EVENT_CAPABILITY_DROP0</a>

