---
UID: NS:fwpmtypes.FWPM_NET_EVENT2_
title: FWPM_NET_EVENT2 (fwpmtypes.h)
description: Contains information about all event types. (FWPM_NET_EVENT2)
helpviewer_keywords: ["FWPM_NET_EVENT2","FWPM_NET_EVENT2 structure [Filtering]","fwp.fwpm_net_event2","fwpmtypes/FWPM_NET_EVENT2"]
old-location: fwp\fwpm_net_event2.htm
tech.root: fwp
ms.assetid: fbcacfb1-b471-474e-bdee-12a481fadc63
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT2, FWPM_NET_EVENT2 structure [Filtering], fwp.fwpm_net_event2, fwpmtypes/FWPM_NET_EVENT2
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
req.typenames: FWPM_NET_EVENT2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_NET_EVENT2_
 - fwpmtypes/FWPM_NET_EVENT2_
 - FWPM_NET_EVENT2
 - fwpmtypes/FWPM_NET_EVENT2
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
 - FWPM_NET_EVENT2
---

# FWPM_NET_EVENT2 structure


## -description

The **FWPM_NET_EVENT2** structure contains information about all event types.
[FWPM_NET_EVENT0](ns-fwpmtypes-fwpm_net_event0.md) is available.

## -struct-fields

### -field header

Type: **[FWPM_NET_EVENT_HEADER2](ns-fwpmtypes-fwpm_net_event_header2.md)**

Information common to all events.

### -field type

Type: **[FWPM_NET_EVENT_TYPE](ne-fwpmtypes-fwpm_net_event_type.md)**

The type of event.

### -field ikeMmFailure

Type: **[FWPM_NET_EVENT_IKEEXT_MM_FAILURE1](ns-fwpmtypes-fwpm_net_event_ikeext_mm_failure1.md)***

Information about  an IKE main mode failure.

Available when **type** is **FWPM_NET_EVENT_TYPE_IKEEXT_MM_FAILURE**.

### -field ikeQmFailure

Type: **[FWPM_NET_EVENT_IKEEXT_QM_FAILURE0](ns-fwpmtypes-fwpm_net_event_ikeext_qm_failure0.md)***

Information about  an IKE quick mode failure.

Available when **type** is **FWPM_NET_EVENT_TYPE_IKEEXT_QM_FAILURE**.

### -field ikeEmFailure

Type: **[FWPM_NET_EVENT_IKEEXT_EM_FAILURE1](ns-fwpmtypes-fwpm_net_event_ikeext_em_failure1.md)***

Information about  an IKE user mode failure.

Available when **type** is **FWPM_NET_EVENT_TYPE_IKEEXT_EM_FAILURE**.

### -field classifyDrop

Type: **[FWPM_NET_EVENT_CLASSIFY_DROP2](ns-fwpmtypes-fwpm_net_event_classify_drop2.md)***

Information about  a drop event.

Available when **type** is **FWPM_NET_EVENT_TYPE_CLASSIFY_DROP**.

### -field ipsecDrop

Type: **[FWPM_NET_EVENT_IPSEC_KERNEL_DROP0](ns-fwpmtypes-fwpm_net_event_ipsec_kernel_drop0.md)***

Information about an IPsec kernel drop event.

Available when **type** is **FWPM_NET_EVENT_TYPE_IPSEC_KERNEL_DROP**.

### -field idpDrop

Type: **[FWPM_NET_EVENT_IPSEC_DOSP_DROP0](ns-fwpmtypes-fwpm_net_event_ipsec_dosp_drop0.md)***

Information about an IPsec DoS Protection event.

Available when **type** is **FWPM_NET_EVENT_IPSEC_DOSP_DROP**.

### -field classifyAllow

Type: **[FWPM_NET_EVENT_CLASSIFY_ALLOW0](ns-fwpmtypes-fwpm_net_event_classify_allow0.md)***

Information about an allow event.

### -field capabilityDrop

Type: **[FWPM_NET_EVENT_CAPABILITY_DROP0](ns-fwpmtypes-fwpm_net_event_capability_drop0.md)***

Information about a capability-related drop event.

### -field capabilityAllow

Type: **[FWPM_NET_EVENT_CAPABILITY_ALLOW0](ns-fwpmtypes-fwpm_net_event_capability_allow0.md)***

Information about a capability-related allow event.

### -field classifyDropMac

Type: **[FWPM_NET_EVENT_CLASSIFY_DROP_MAC0](ns-fwpmtypes-fwpm_net_event_classify_drop_mac0.md)***

Information about a MAC layer drop event.

## -see-also

[Windows Filtering Platform  API Structures](/windows/desktop/FWP/fwp-structs)
