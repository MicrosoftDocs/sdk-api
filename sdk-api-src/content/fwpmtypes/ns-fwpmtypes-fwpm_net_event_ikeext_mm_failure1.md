---
UID: NS:fwpmtypes.FWPM_NET_EVENT_IKEEXT_MM_FAILURE1_
title: FWPM_NET_EVENT_IKEEXT_MM_FAILURE1 (fwpmtypes.h)
description: Contains information that describes an IKE/AuthIP Main Mode (MM) failure. (FWPM_NET_EVENT_IKEEXT_MM_FAILURE1)
helpviewer_keywords: ["FWPM_NET_EVENT_IKEEXT_MM_FAILURE1","FWPM_NET_EVENT_IKEEXT_MM_FAILURE1 structure [Filtering]","FWPM_NET_EVENT_IKEEXT_MM_FAILURE_FLAG_BENIGN","FWPM_NET_EVENT_IKEEXT_MM_FAILURE_FLAG_MULTIPLE","fwp.fwpm_net_event_ikeext_mm_failure1","fwpmtypes/FWPM_NET_EVENT_IKEEXT_MM_FAILURE1"]
old-location: fwp\fwpm_net_event_ikeext_mm_failure1.htm
tech.root: fwp
ms.assetid: 4c67353c-289c-42ef-9081-20c33a9a06a4
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_IKEEXT_MM_FAILURE1, FWPM_NET_EVENT_IKEEXT_MM_FAILURE1 structure [Filtering], FWPM_NET_EVENT_IKEEXT_MM_FAILURE_FLAG_BENIGN, FWPM_NET_EVENT_IKEEXT_MM_FAILURE_FLAG_MULTIPLE, fwp.fwpm_net_event_ikeext_mm_failure1, fwpmtypes/FWPM_NET_EVENT_IKEEXT_MM_FAILURE1
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
req.typenames: FWPM_NET_EVENT_IKEEXT_MM_FAILURE1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_NET_EVENT_IKEEXT_MM_FAILURE1_
 - fwpmtypes/FWPM_NET_EVENT_IKEEXT_MM_FAILURE1_
 - FWPM_NET_EVENT_IKEEXT_MM_FAILURE1
 - fwpmtypes/FWPM_NET_EVENT_IKEEXT_MM_FAILURE1
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
 - FWPM_NET_EVENT_IKEEXT_MM_FAILURE1
---

# FWPM_NET_EVENT_IKEEXT_MM_FAILURE1 structure


## -description

The **FWPM_NET_EVENT_IKEEXT_MM_FAILURE1** structure contains information that describes an IKE/AuthIP Main Mode (MM) failure.
[FWPM_NET_EVENT_IKEEXT_MM_FAILURE0](ns-fwpmtypes-fwpm_net_event_ikeext_mm_failure0.md) is available.

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

### -field localPrincipalNameForAuth

Name of the MM local security principal.

### -field remotePrincipalNameForAuth

Name of the MM remote security principal.

### -field numLocalPrincipalGroupSids

Number of groups in the local security principal's token.

### -field localPrincipalGroupSids

Groups in the local security principal's token.

### -field numRemotePrincipalGroupSids

Number of groups in the remote security principal's token.

### -field remotePrincipalGroupSids

Groups in the remote security principal's token.

## -see-also

[Windows Filtering Platform  API Structures](/windows/desktop/FWP/fwp-structs)
