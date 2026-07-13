---
UID: NS:fwpmtypes.FWPM_NET_EVENT4_
title: FWPM_NET_EVENT4
description: Contains information about all event types. FWPM_NET_EVENT3 and FWPM_NET_EVENT2 are available. For Windows 7, FWPM_NET_EVENT1 is available. For Windows Vista, FWPM_NET_EVENT0 is available.
tech.root: fwp
ms.date: 04/12/2024
targetos: Windows
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: fwpmtypes.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: FWPM_NET_EVENT4
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - fwpmtypes.h
api_name:
 - FWPM_NET_EVENT4_
 - FWPM_NET_EVENT4
f1_keywords:
 - FWPM_NET_EVENT4_
 - fwpmtypes/FWPM_NET_EVENT4_
 - FWPM_NET_EVENT4
 - fwpmtypes/FWPM_NET_EVENT4
dev_langs:
 - c++
helpviewer_keywords:
 - FWPM_NET_EVENT4_
---

## -description

The **FWPM_NET_EVENT4** structure contains information about all event types. [FWPM_NET_EVENT3](ns-fwpmtypes-fwpm_net_event3.md) and [FWPM_NET_EVENT2](ns-fwpmtypes-fwpm_net_event2.md) are available. For Windows 7, [FWPM_NET_EVENT1](ns-fwpmtypes-fwpm_net_event1.md) is available. For Windows Vista, [FWPM_NET_EVENT0](ns-fwpmtypes-fwpm_net_event0.md) is available.

## -struct-fields

### -field header

Information common to all events.

### -field type

The type of event.

### -field ikeMmFailure

Information about an IKE main mode failure.

Available when **type** is **FWPM_NET_EVENT_TYPE_IKEEXT_MM_FAILURE**.

### -field ikeQmFailure

Information about an IKE quick mode failure.

Available when **type** is **FWPM_NET_EVENT_TYPE_IKEEXT_QM_FAILURE**.

### -field ikeEmFailure

Information about an IKE user mode failure.

Available when **type** is **FWPM_NET_EVENT_TYPE_IKEEXT_EM_FAILURE**.

### -field classifyDrop

Information about a drop event.

Available when **type** is **FWPM_NET_EVENT_TYPE_CLASSIFY_DROP**.

### -field ipsecDrop

Information about an IPsec kernel drop event.

Available when **type** is **FWPM_NET_EVENT_TYPE_IPSEC_KERNEL_DROP**.

### -field idpDrop

Information about an IPsec DoS Protection event.

Available when **type** is **FWPM_NET_EVENT_IPSEC_DOSP_DROP**.

### -field classifyAllow

Information about an allow event.

### -field capabilityDrop

Information about a capability-related drop event.

### -field capabilityAllow

Information about a capability-related allow event.

### -field classifyDropMac

Information about a MAC layer drop event.

## -remarks

## -see-also

[Windows Filtering Platform API structures](/windows/desktop/FWP/fwp-structs)
