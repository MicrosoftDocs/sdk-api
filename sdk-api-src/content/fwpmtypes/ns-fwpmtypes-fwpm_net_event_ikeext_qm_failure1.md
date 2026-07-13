---
UID: NS:fwpmtypes.FWPM_NET_EVENT_IKEEXT_QM_FAILURE1_
title: FWPM_NET_EVENT_IKEEXT_QM_FAILURE1
description: Contains information that describes an IKE/AuthIP Quick Mode (QM) failure. FWPM_NET_EVENT_IKEEXT_QM_FAILURE0 is also available.
tech.root: fwp
ms.date: 04/25/2024
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
req.typenames: FWPM_NET_EVENT_IKEEXT_QM_FAILURE1
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
 - FWPM_NET_EVENT_IKEEXT_QM_FAILURE1_
 - FWPM_NET_EVENT_IKEEXT_QM_FAILURE1
f1_keywords:
 - FWPM_NET_EVENT_IKEEXT_QM_FAILURE1_
 - fwpmtypes/FWPM_NET_EVENT_IKEEXT_QM_FAILURE1_
 - FWPM_NET_EVENT_IKEEXT_QM_FAILURE1
 - fwpmtypes/FWPM_NET_EVENT_IKEEXT_QM_FAILURE1
dev_langs:
 - c++
helpviewer_keywords:
 - FWPM_NET_EVENT_IKEEXT_QM_FAILURE1_
---

## -description

Contains information that describes an IKE/AuthIP Quick Mode (QM) failure. [FWPM_NET_EVENT_IKEEXT_QM_FAILURE0](./ns-fwpmtypes-fwpm_net_event_ikeext_qm_failure0.md) is also available.

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

### -field mmSaLuid

A LUID representing the main mode security association.

### -field mmProviderContextKey

A GUID representing the main mode provider context.

## -remarks

**FWPM_NET_EVENT_IKEEXT_QM_FAILURE1** is a specific implementation of **FWPM_NET_EVENT_IKEEXT_QM_FAILURE**. For more info, see [WFP Version-Independent Names and Targeting Specific Versions of Windows](/windows/win32/fwp/wfp-version-independent-names-and-targeting-specific-versions-of-windows).

## -see-also
