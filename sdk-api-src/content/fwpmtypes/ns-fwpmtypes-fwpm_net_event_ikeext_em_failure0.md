---
UID: NS:fwpmtypes.FWPM_NET_EVENT_IKEEXT_EM_FAILURE0_
title: FWPM_NET_EVENT_IKEEXT_EM_FAILURE0 (fwpmtypes.h)
description: The FWPM_NET_EVENT_IKEEXT_EM_FAILURE0 structure contains information that describes an IKE Extended Mode (EM) failure.Note  FWPM_NET_EVENT_IKEEXT_EM_FAILURE0 is the specific implementation of FWPM_NET_EVENT_IKEEXT_EM_FAILURE used in Windows Vista.
helpviewer_keywords: ["FWPM_NET_EVENT_IKEEXT_EM_FAILURE0","FWPM_NET_EVENT_IKEEXT_EM_FAILURE0 structure [Filtering]","FWPM_NET_EVENT_IKEEXT_EM_FAILURE_FLAG_MULTIPLE","fwp.fwpm_net_event_ikeext_em_failure0","fwpmtypes/FWPM_NET_EVENT_IKEEXT_EM_FAILURE0"]
old-location: fwp\fwpm_net_event_ikeext_em_failure0.htm
tech.root: fwp
ms.assetid: 53b28166-8f19-4891-aeb0-603628d95053
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_IKEEXT_EM_FAILURE0, FWPM_NET_EVENT_IKEEXT_EM_FAILURE0 structure [Filtering], FWPM_NET_EVENT_IKEEXT_EM_FAILURE_FLAG_MULTIPLE, fwp.fwpm_net_event_ikeext_em_failure0, fwpmtypes/FWPM_NET_EVENT_IKEEXT_EM_FAILURE0
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
req.typenames: FWPM_NET_EVENT_IKEEXT_EM_FAILURE0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_NET_EVENT_IKEEXT_EM_FAILURE0_
 - fwpmtypes/FWPM_NET_EVENT_IKEEXT_EM_FAILURE0_
 - FWPM_NET_EVENT_IKEEXT_EM_FAILURE0
 - fwpmtypes/FWPM_NET_EVENT_IKEEXT_EM_FAILURE0
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
 - FWPM_NET_EVENT_IKEEXT_EM_FAILURE0
---

# FWPM_NET_EVENT_IKEEXT_EM_FAILURE0 structure


## -description

The **FWPM_NET_EVENT_IKEEXT_EM_FAILURE0** structure contains information that describes an IKE Extended Mode (EM) failure.
[FWPM_NET_EVENT_IKEEXT_EM_FAILURE1](ns-fwpmtypes-fwpm_net_event_ikeext_em_failure1.md) is available.

## -struct-fields

### -field failureErrorCode

Windows error code for the failure.

### -field failurePoint

An [IPSEC_FAILURE_POINT](../ipsectypes/ne-ipsectypes-ipsec_failure_point.md) value that indicates the IPsec state when the failure occurred.

### -field flags

Flags for the failure event.

| Value | Meaning |
| ----- | ------- |
| FWPM_NET_EVENT_IKEEXT_EM_FAILURE_FLAG_MULTIPLE | Indicates that multiple IKE EM failure events have been reported. |

### -field emState

An [IKEEXT_EM_SA_STATE](../iketypes/ne-iketypes-ikeext_em_sa_state.md) value that indicates the EM state when the failure occurred.

### -field saRole

An [IKEEXT_SA_ROLE](../iketypes/ne-iketypes-ikeext_sa_role.md) value that specifies the SA role when the failure occurred.

### -field emAuthMethod

An [IKEEXT_AUTHENTICATION_METHOD_TYPE](../iketypes/ne-iketypes-ikeext_authentication_method_type.md) value that specifies the authentication method.

### -field endCertHash

SHA thumbprint hash of the end certificate corresponding to the failures that happen during building or validating certificate chains.

**IKEEXT_CERT_HASH_LEN** maps to 20.

### -field mmId

LUID for the Main Mode (MM) SA.

### -field qmFilterId

Quick Mode (QM) filter ID associated with this failure.

## -see-also

[IKEEXT_AUTHENTICATION_METHOD_TYPE](../iketypes/ne-iketypes-ikeext_authentication_method_type.md)

[IKEEXT_EM_SA_STATE](../iketypes/ne-iketypes-ikeext_em_sa_state.md)

[IKEEXT_SA_ROLE](../iketypes/ne-iketypes-ikeext_sa_role.md)

[IPSEC_FAILURE_POINT](../ipsectypes/ne-ipsectypes-ipsec_failure_point.md)

[Windows Filtering Platform  API Structures](/windows/desktop/FWP/fwp-structs)
