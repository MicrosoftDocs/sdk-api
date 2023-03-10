---
UID: NS:fwpmtypes.FWPM_NET_EVENT3_
title: FWPM_NET_EVENT3 (fwpmtypes.h)
description: Contains information about all event types. (FWPM_NET_EVENT3)
old-location: fwp\fwpm_net_event3.htm
tech.root: fwp
ms.assetid: 2D71C44C-B553-46DD-8943-DCC979A7DC6B
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT3, FWPM_NET_EVENT3 structure [Filtering], fwp.fwpm_net_event3, fwpmtypes/FWPM_NET_EVENT3
f1_keywords:
- fwpmtypes/FWPM_NET_EVENT3
dev_langs:
- c++
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Fwpmtypes.h
api_name:
- FWPM_NET_EVENT3
targetos: Windows
req.typenames: FWPM_NET_EVENT3
req.redist: 
ms.custom: 19H1
---

# FWPM_NET_EVENT3 structure


## -description


The **FWPM_NET_EVENT3** structure contains information about all event types.
[FWPM_NET_EVENT2](ns-fwpmtypes-fwpm_net_event2.md) is available. For Windows 7, [FWPM_NET_EVENT1](ns-fwpmtypes-fwpm_net_event1.md) is available. For Windows Vista, [FWPM_NET_EVENT0](ns-fwpmtypes-fwpm_net_event0.md) is available.

## -struct-fields

### -field header

Information common to all events.

### -field type

The type of event.

### -field ikeMmFailure

Information about  an IKE main mode failure.

Available when **type** is **FWPM_NET_EVENT_TYPE_IKEEXT_MM_FAILURE**.

### -field ikeQmFailure

Information about  an IKE quick mode failure.

Available when **type** is **FWPM_NET_EVENT_TYPE_IKEEXT_QM_FAILURE**.

### -field ikeEmFailure

Information about  an IKE user mode failure.

Available when **type** is **FWPM_NET_EVENT_TYPE_IKEEXT_EM_FAILURE**.

### -field classifyDrop

Information about  a drop event.

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

## -see-also

[Windows Filtering Platform  API Structures](/windows/desktop/FWP/fwp-structs)
