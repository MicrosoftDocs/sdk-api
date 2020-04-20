---
UID: NS:fwpmtypes.FWPM_NET_EVENT2_
title: FWPM_NET_EVENT2 (fwpmtypes.h)
description: Contains information about all event types.helpviewer_keywords: ["FWPM_NET_EVENT2","FWPM_NET_EVENT2 structure [Filtering]","fwp.fwpm_net_event2","fwpmtypes/FWPM_NET_EVENT2"]
old-location: fwp\fwpm_net_event2.htm
tech.root: fwp
ms.assetid: fbcacfb1-b471-474e-bdee-12a481fadc63
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT2, FWPM_NET_EVENT2 structure [Filtering], fwp.fwpm_net_event2, fwpmtypes/FWPM_NET_EVENT2
f1_keywords:
- fwpmtypes/FWPM_NET_EVENT2
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Fwpmtypes.h
api_name:
- FWPM_NET_EVENT2
targetos: Windows
req.typenames: FWPM_NET_EVENT2
req.redist: 
ms.custom: 19H1
---

# FWPM_NET_EVENT2 structure


## -description


The <b>FWPM_NET_EVENT2</b> structure contains information about all event types.
[FWPM_NET_EVENT0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event0)a> is available.</div><div> </div>

## -struct-fields




### -field header

Type: [FWPM_NET_EVENT_HEADER2](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2)a></b>

Information common to all events.


### -field type

Type: [FWPM_NET_EVENT_TYPE](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_net_event_type)a></b>

The type of event.


### -field ikeMmFailure

Type: <b><a href="https://docs.microsoft.com/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_mm_failure1">FWPM_NET_EVENT_IKEEXT_MM_FAILURE1</a>*</b>

Information about  an IKE main mode failure.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_IKEEXT_MM_FAILURE</b>.


### -field ikeQmFailure

Type: <b><a href="https://docs.microsoft.com/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_qm_failure0">FWPM_NET_EVENT_IKEEXT_QM_FAILURE0</a>*</b>

Information about  an IKE quick mode failure.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_IKEEXT_QM_FAILURE</b>.


### -field ikeEmFailure

Type: <b><a href="https://docs.microsoft.com/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_em_failure1">FWPM_NET_EVENT_IKEEXT_EM_FAILURE1</a>*</b>

Information about  an IKE user mode failure.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_IKEEXT_EM_FAILURE</b>.


### -field classifyDrop

Type: [FWPM_NET_EVENT_CLASSIFY_DROP2](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop2)a>*</b>

Information about  a drop event.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_CLASSIFY_DROP</b>.


### -field ipsecDrop

Type: <b><a href="https://docs.microsoft.com/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_ipsec_kernel_drop0">FWPM_NET_EVENT_IPSEC_KERNEL_DROP0</a>*</b>

Information about an IPsec kernel drop event.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_IPSEC_KERNEL_DROP</b>.


### -field idpDrop

Type: <b><a href="https://docs.microsoft.com/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_ipsec_dosp_drop0">FWPM_NET_EVENT_IPSEC_DOSP_DROP0</a>*</b>

Information about an IPsec DoS Protection event.

Available when <b>type</b> is <b>FWPM_NET_EVENT_IPSEC_DOSP_DROP</b>.


### -field classifyAllow

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_allow0">FWPM_NET_EVENT_CLASSIFY_ALLOW0</a>*</b>

Information about an allow event.


### -field capabilityDrop

Type: <b><a href="https://docs.microsoft.com/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_drop0">FWPM_NET_EVENT_CAPABILITY_DROP0</a>*</b>

Information about a capability-related drop event.


### -field capabilityAllow

Type: <b><a href="https://docs.microsoft.com/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_allow0">FWPM_NET_EVENT_CAPABILITY_ALLOW0</a>*</b>

Information about a capability-related allow event.


### -field classifyDropMac

Type: <b><a href="https://docs.microsoft.com/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop_mac0">FWPM_NET_EVENT_CLASSIFY_DROP_MAC0</a>*</b>

Information about a MAC layer drop event.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

