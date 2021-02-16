---
UID: NS:fwpmtypes.FWPM_NET_EVENT_CAPABILITY_DROP0_
title: FWPM_NET_EVENT_CAPABILITY_DROP0 (fwpmtypes.h)
description: Contains information about network traffic dropped in relation to an app container network capability.
helpviewer_keywords: ["FWPM_NET_EVENT_CAPABILITY_DROP0","FWPM_NET_EVENT_CAPABILITY_DROP0 structure [Filtering]","fwp.fwpm_net_event_capability_drop0","fwpmtypes/FWPM_NET_EVENT_CAPABILITY_DROP0"]
old-location: fwp\fwpm_net_event_capability_drop0.htm
tech.root: fwp
ms.assetid: 40848332-0961-417c-8adc-dd1a380594ba
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_CAPABILITY_DROP0, FWPM_NET_EVENT_CAPABILITY_DROP0 structure [Filtering], fwp.fwpm_net_event_capability_drop0, fwpmtypes/FWPM_NET_EVENT_CAPABILITY_DROP0
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
req.typenames: FWPM_NET_EVENT_CAPABILITY_DROP0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_NET_EVENT_CAPABILITY_DROP0_
 - fwpmtypes/FWPM_NET_EVENT_CAPABILITY_DROP0_
 - FWPM_NET_EVENT_CAPABILITY_DROP0
 - fwpmtypes/FWPM_NET_EVENT_CAPABILITY_DROP0
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
 - FWPM_NET_EVENT_CAPABILITY_DROP0
---

# FWPM_NET_EVENT_CAPABILITY_DROP0 structure


## -description

The <b>FWPM_NET_EVENT_CAPABILITY_DROP0</b> structure contains information about network traffic dropped  in relation to an app container network capability. Traffic is dropped due to the specified app container network capability and enforced by  the specified filter identifier.

## -struct-fields

### -field networkCapabilityId

Type: <b><a href="/windows/win32/api/fwpmtypes/ne-fwpmtypes-fwpm_appc_network_capability_type">FWPM_APPC_NETWORK_CAPABILITY_TYPE</a></b>

The specific app container network capability which was missing, therefore causing this traffic to be denied.

### -field filterId

Type: <b>UINT64</b>

A LUID identifying the WFP filter where the traffic drop occurred.

### -field isLoopback

Type: <b>BOOL</b>

True if the packet originated from (or was heading to) the loopback adapter; otherwise, false.

## -see-also

<a href="/windows/win32/api/fwpmtypes/ne-fwpmtypes-fwpm_appc_network_capability_type">FWPM_APPC_NETWORK_CAPABILITY_TYPE</a>



<a href="/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_allow0">FWPM_NET_EVENT_CAPABILITY_ALLOW0</a>

