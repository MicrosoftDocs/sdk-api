---
UID: NS:fwpmtypes.FWPM_NET_EVENT1_
title: FWPM_NET_EVENT1 (fwpmtypes.h)
description: Contains information about all event types. (FWPM_NET_EVENT1)
helpviewer_keywords: ["FWPM_NET_EVENT1","FWPM_NET_EVENT1 structure [Filtering]","fwp.fwpm_net_event1","fwpmtypes/FWPM_NET_EVENT1"]
old-location: fwp\fwpm_net_event1.htm
tech.root: fwp
ms.assetid: 0f989f66-8373-4546-ade3-8b337c4507e2
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT1, FWPM_NET_EVENT1 structure [Filtering], fwp.fwpm_net_event1, fwpmtypes/FWPM_NET_EVENT1
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: FWPM_NET_EVENT1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_NET_EVENT1_
 - fwpmtypes/FWPM_NET_EVENT1_
 - FWPM_NET_EVENT1
 - fwpmtypes/FWPM_NET_EVENT1
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
 - FWPM_NET_EVENT1
---

# FWPM_NET_EVENT1 structure


## -description

The **FWPM_NET_EVENT1** structure contains information about all event types.
[FWPM_NET_EVENT0](ns-fwpmtypes-fwpm_net_event0.md) is available.

## -struct-fields

### -field header

An [FWPM_NET_EVENT_HEADER1](ns-fwpmtypes-fwpm_net_event_header1.md) structure that contains information common to all events.

### -field type

An [FWPM_NET_EVENT_TYPE](ne-fwpmtypes-fwpm_net_event_type.md) value that specifies the type of event.

### -field ikeMmFailure

Address of an [FWPM_NET_EVENT_IKEEXT_MM_FAILURE1](ns-fwpmtypes-fwpm_net_event_ikeext_mm_failure1.md) structure that contains information about  an IKE main mode failure.

Available when **type** is **FWPM_NET_EVENT_TYPE_IKEEXT_MM_FAILURE**.

### -field ikeQmFailure

Address of an [FWPM_NET_EVENT_IKEEXT_QM_FAILURE0](ns-fwpmtypes-fwpm_net_event_ikeext_qm_failure0.md) structure that contains information about  an IKE quick mode failure.

Available when **type** is **FWPM_NET_EVENT_TYPE_IKEEXT_QM_FAILURE**.

### -field ikeEmFailure

Address of an [FWPM_NET_EVENT_IKEEXT_EM_FAILURE1](ns-fwpmtypes-fwpm_net_event_ikeext_em_failure1.md) structure that contains information about  an IKE user mode failure.

Available when **type** is **FWPM_NET_EVENT_TYPE_IKEEXT_EM_FAILURE**.

### -field classifyDrop

Address of an [FWPM_NET_EVENT_CLASSIFY_DROP1](ns-fwpmtypes-fwpm_net_event_classify_drop1.md) structure that contains information about  a drop event.

Available when **type** is **FWPM_NET_EVENT_TYPE_CLASSIFY_DROP**.

### -field ipsecDrop

Address of an [FWPM_NET_EVENT_IPSEC_KERNEL_DROP0](ns-fwpmtypes-fwpm_net_event_ipsec_kernel_drop0.md) structure that contains information about an IPsec kernel drop event.

Available when **type** is **FWPM_NET_EVENT_TYPE_IPSEC_KERNEL_DROP**.

### -field idpDrop

Address of an [FWPM_NET_EVENT_IPSEC_DOSP_DROP0](ns-fwpmtypes-fwpm_net_event_ipsec_dosp_drop0.md) structure that contains information about an IPsec DoS Protection event.

Available when **type** is **FWPM_NET_EVENT_IPSEC_DOSP_DROP**.

## -see-also

[Windows Filtering Platform  API Structures](/windows/desktop/FWP/fwp-structs)
