---
UID: NS:fwpmtypes.FWPM_NET_EVENT_IKEEXT_MM_FAILURE0_
title: FWPM_NET_EVENT_IKEEXT_MM_FAILURE0 (fwpmtypes.h)
description: Contains information that describes an IKE/AuthIP Main Mode (MM) failure. (FWPM_NET_EVENT_IKEEXT_MM_FAILURE0)
helpviewer_keywords: ["FWPM_NET_EVENT_IKEEXT_MM_FAILURE0","FWPM_NET_EVENT_IKEEXT_MM_FAILURE0 structure [Filtering]","FWPM_NET_EVENT_IKEEXT_MM_FAILURE_FLAG_BENIGN","FWPM_NET_EVENT_IKEEXT_MM_FAILURE_FLAG_MULTIPLE","fwp.fwpm_net_event_ikeext_mm_failure0","fwpmtypes/FWPM_NET_EVENT_IKEEXT_MM_FAILURE0"]
old-location: fwp\fwpm_net_event_ikeext_mm_failure0.htm
tech.root: fwp
ms.assetid: 66845a68-e465-44d9-afc0-3d95b10cc69f
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_IKEEXT_MM_FAILURE0, FWPM_NET_EVENT_IKEEXT_MM_FAILURE0 structure [Filtering], FWPM_NET_EVENT_IKEEXT_MM_FAILURE_FLAG_BENIGN, FWPM_NET_EVENT_IKEEXT_MM_FAILURE_FLAG_MULTIPLE, fwp.fwpm_net_event_ikeext_mm_failure0, fwpmtypes/FWPM_NET_EVENT_IKEEXT_MM_FAILURE0
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
req.typenames: FWPM_NET_EVENT_IKEEXT_MM_FAILURE0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_NET_EVENT_IKEEXT_MM_FAILURE0_
 - fwpmtypes/FWPM_NET_EVENT_IKEEXT_MM_FAILURE0_
 - FWPM_NET_EVENT_IKEEXT_MM_FAILURE0
 - fwpmtypes/FWPM_NET_EVENT_IKEEXT_MM_FAILURE0
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
 - FWPM_NET_EVENT_IKEEXT_MM_FAILURE0
---

# FWPM_NET_EVENT_IKEEXT_MM_FAILURE0 structure


## -description

The **FWPM_NET_EVENT_IKEEXT_MM_FAILURE0** structure contains information that describes an IKE/AuthIP Main Mode (MM) failure.
[FWPM_NET_EVENT_IKEEXT_MM_FAILURE1](ns-fwpmtypes-fwpm_net_event_ikeext_mm_failure1.md) is available.

## -struct-fields

### -field failureErrorCode

Windows error code for the failure.

### -field failurePoint

An [IPSEC_FAILURE_POINT](../ipsectypes/ne-ipsectypes-ipsec_failure_point.md) value that indicates the IPsec state when the failure occurred.

### -field flags

Flags for the failure event.

| Value | Meaning |
| ----- | ------- |
| FWPM_NET_EVENT_IKEEXT_MM_FAILURE_FLAG_BENIGN | Indicates that the failure was benign or expected. |
| FWPM_NET_EVENT_IKEEXT_MM_FAILURE_FLAG_MULTIPLE | Indicates that multiple failure events have been reported. |

### -field keyingModuleType

 An [IKEEXT_KEY_MODULE_TYPE](../iketypes/ne-iketypes-ikeext_key_module_type.md) value that specifies the type of keying module.

### -field mmState

An [IKEEXT_MM_SA_STATE](../iketypes/ne-iketypes-ikeext_mm_sa_state.md) value that indicates the Main Mode state when the failure occurred.

### -field saRole

An [IKEEXT_SA_ROLE](../iketypes/ne-iketypes-ikeext_sa_role.md) value that specifies the security association (SA) role when the failure occurred.

### -field mmAuthMethod

An [IKEEXT_AUTHENTICATION_METHOD_TYPE](../iketypes/ne-iketypes-ikeext_authentication_method_type.md) value that specifies the authentication method.

### -field endCertHash

SHA thumbprint hash of the end certificate corresponding to the failures that happen during building or validating certificate chains.

**IKEEXT_CERT_HASH_LEN** maps to 20.

### -field mmId

LUID for the MM SA.

### -field mmFilterId

Main mode filter ID.

## -see-also

[Windows Filtering Platform  API Structures](/windows/desktop/FWP/fwp-structs)
