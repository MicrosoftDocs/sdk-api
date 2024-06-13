---
UID: NS:fwpmtypes.FWPM_NET_EVENT_IKEEXT_QM_FAILURE0_
title: FWPM_NET_EVENT_IKEEXT_QM_FAILURE0 (fwpmtypes.h)
description: Contains information that describes an IKE/AuthIP Quick Mode (QM) failure.
helpviewer_keywords: ["FWPM_NET_EVENT_IKEEXT_QM_FAILURE0","FWPM_NET_EVENT_IKEEXT_QM_FAILURE0 structure [Filtering]","fwp.fwpm_net_event_ikeext_qm_failure0","fwpmtypes/FWPM_NET_EVENT_IKEEXT_QM_FAILURE0"]
old-location: fwp\fwpm_net_event_ikeext_qm_failure0.htm
tech.root: fwp
ms.assetid: a9cffcee-67a2-4a04-9ff1-85e2e02fa9a9
ms.date: 04/25/2024
ms.keywords: FWPM_NET_EVENT_IKEEXT_QM_FAILURE0, FWPM_NET_EVENT_IKEEXT_QM_FAILURE0 structure [Filtering], fwp.fwpm_net_event_ikeext_qm_failure0, fwpmtypes/FWPM_NET_EVENT_IKEEXT_QM_FAILURE0
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: FWPM_NET_EVENT_IKEEXT_QM_FAILURE0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_NET_EVENT_IKEEXT_QM_FAILURE0_
 - fwpmtypes/FWPM_NET_EVENT_IKEEXT_QM_FAILURE0_
 - FWPM_NET_EVENT_IKEEXT_QM_FAILURE0
 - fwpmtypes/FWPM_NET_EVENT_IKEEXT_QM_FAILURE0
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
 - FWPM_NET_EVENT_IKEEXT_QM_FAILURE0
---

## -description

The <b>FWPM_NET_EVENT_IKEEXT_QM_FAILURE0</b> structure contains information that describes an IKE/AuthIP Quick Mode (QM) failure.

## -struct-fields

### -field failureErrorCode

Windows error code for the failure.

### -field failurePoint

An [IPSEC_FAILURE_POINT](/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_failure_point) value that indicates the IPsec state when the failure occurred.

### -field keyingModuleType

 An [IKEEXT_KEY_MODULE_TYPE](/windows/desktop/api/iketypes/ne-iketypes-ikeext_key_module_type) value that specifies the type of keying module.

### -field qmState

An [IKEEXT_QM_SA_STATE](/windows/desktop/api/iketypes/ne-iketypes-ikeext_qm_sa_state) value that specifies the QM state when the failure occurred.

### -field saRole

An [IKEEXT_SA_ROLE](/windows/desktop/api/iketypes/ne-iketypes-ikeext_sa_role) value that specifies the SA role when the failure occurred.

### -field saTrafficType

 An [IPSEC_TRAFFIC_TYPE](/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_traffic_type) value that specifies the type of traffic.

### -field localSubNet

An [FWP_CONDITION_VALUE0](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_condition_value0) structure that contains values that conditions can use when testing for matches.

Available when <b>saTrafficType</b> is <b>IPSEC_TRAFFIC_TYPE_TUNNEL</b>.

### -field remoteSubNet

An [FWP_CONDITION_VALUE0](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_condition_value0) structure that contains values that conditions can use when testing for matches.

Available when <b>saTrafficType</b> is <b>IPSEC_TRAFFIC_TYPE_TUNNEL</b>.

### -field qmFilterId

Quick Mode filter ID.

## -remarks

**FWPM_NET_EVENT_IKEEXT_QM_FAILURE0** is a specific implementation of **FWPM_NET_EVENT_IKEEXT_QM_FAILURE**. For more info, see [WFP Version-Independent Names and Targeting Specific Versions of Windows](/windows/win32/fwp/wfp-version-independent-names-and-targeting-specific-versions-of-windows).

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform API Structures</a>
