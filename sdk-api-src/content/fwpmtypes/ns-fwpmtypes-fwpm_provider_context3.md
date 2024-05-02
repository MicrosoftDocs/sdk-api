---
UID: NS:fwpmtypes.FWPM_PROVIDER_CONTEXT3_
title: FWPM_PROVIDER_CONTEXT3
description: Stores the state associated with a provider context. FWPM_PROVIDER_CONTEXT0, FWPM_PROVIDER_CONTEXT1, and FWPM_PROVIDER_CONTEXT2 are available.
tech.root: fwp
ms.date: 04/26/2024
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
req.typenames: FWPM_PROVIDER_CONTEXT3
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
 - FWPM_PROVIDER_CONTEXT3_
 - FWPM_PROVIDER_CONTEXT3
f1_keywords:
 - FWPM_PROVIDER_CONTEXT3_
 - fwpmtypes/FWPM_PROVIDER_CONTEXT3_
 - FWPM_PROVIDER_CONTEXT3
 - fwpmtypes/FWPM_PROVIDER_CONTEXT3
dev_langs:
 - c++
helpviewer_keywords:
 - FWPM_PROVIDER_CONTEXT3_
---

## -description

Stores the state associated with a provider context. [FWPM_PROVIDER_CONTEXT0](./ns-fwpmtypes-fwpm_provider_context0.md), [FWPM_PROVIDER_CONTEXT1](./ns-fwpmtypes-fwpm_provider_context1.md), and [FWPM_PROVIDER_CONTEXT2](./ns-fwpmtypes-fwpm_provider_context2.md) are available.

## -struct-fields

### -field providerContextKey

Type: **GUID**

Uniquely identifies the provider context. If the GUID is zero-initialized in the call to [FwpmProviderContextAdd2](../fwpmu/nf-fwpmu-fwpmprovidercontextadd2.md), then Base Filtering Engine (BFE) will generate one.

### -field displayData

Type: **[FWPM_DISPLAY_DATA0](../fwptypes/ns-fwptypes-fwpm_display_data0.md)**

Allows provider contexts to be annotated in a human-readable form. The [FWPM_DISPLAY_DATA0](../fwptypes/ns-fwptypes-fwpm_display_data0.md) structure is required.

### -field flags

Type: **UINT32**

Possible values:

| Provider context flag | Meaning |
| - | - |
| FWPM_PROVIDER_CONTEXT_FLAG_PERSISTENT | The object is persistent, that is, it survives across BFE stop/start. |
| FWPM_PROVIDER_CONTEXT_FLAG_DOWNLEVEL | Reserved for internal use. |

### -field providerKey

Type: **GUID\***

GUID of the policy provider that manages this object.

### -field providerData

Type: **[FWP_BYTE_BLOB](../fwptypes/ns-fwptypes-fwp_byte_blob.md)**

Optional provider-specific data that allows providers to store additional context info with the object.

### -field type

Type: **[FWPM_PROVIDER_CONTEXT_TYPE](ne-fwpmtypes-fwpm_provider_context_type.md)**

The type of provider context.

### -field keyingPolicy

Type: **[IPSEC_KEYING_POLICY1](../ipsectypes/ns-ipsectypes-ipsec_keying_policy1.md)\***

Available when **type** is **FWPM_IPSEC_KEYING_CONTEXT**.

### -field ikeQmTransportPolicy

Type: **[IPSEC_TRANSPORT_POLICY2](../ipsectypes/ns-ipsectypes-ipsec_transport_policy2.md)\***

Available when **type** is **FWPM_IPSEC_IKE_QM_TRANSPORT_CONTEXT**.

### -field ikeQmTunnelPolicy

Type: **[IPSEC_TUNNEL_POLICY2](../ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2.md)\***

Available when **type** is **FWPM_IPSEC_IKE_QM_TUNNEL_CONTEXT**.

### -field authipQmTransportPolicy

Type: **[IPSEC_TRANSPORT_POLICY2](../ipsectypes/ns-ipsectypes-ipsec_transport_policy2.md)\***

 [case()][unique]

### -field authipQmTunnelPolicy

Type: **[IPSEC_TUNNEL_POLICY2](../ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2.md)\***

Available when **type** is **FWPM_IPSEC_AUTHIP_QM_TRANSPORT_CONTEXT**.

### -field ikeMmPolicy

Type: **[IKEEXT_POLICY2](../iketypes/ns-iketypes-ikeext_policy2.md)\***

Available when **type** is **FWPM_IPSEC_IKE_MM_CONTEXT**.

### -field authIpMmPolicy

Type: **[IKEEXT_POLICY2](../iketypes/ns-iketypes-ikeext_policy2.md)\***

Available when **type** is **FWPM_IPSEC_AUTHIP_MM_CONTEXT**.

### -field dataBuffer

Type: **[FWP_BYTE_BLOB](../fwptypes/ns-fwptypes-fwp_byte_blob.md)\***

Available when **type** is **FWPM_GENERAL_CONTEXT**.

### -field classifyOptions

Type: **[FWPM_CLASSIFY_OPTIONS0](ns-fwpmtypes-fwpm_classify_options0.md)\***

Available when **type** is **FWPM_CLASSIFY_OPTIONS_CONTEXT**.

### -field ikeV2QmTunnelPolicy

Type: **[IPSEC_TUNNEL_POLICY2](../ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2.md)\***

Available when **type** is **FWPM_IPSEC_IKEV2_QM_TUNNEL_CONTEXT**.

### -field ikeV2QmTransportPolicy

Type: **[IPSEC_TRANSPORT_POLICY2](../ipsectypes/ns-ipsectypes-ipsec_transport_policy2.md)\***

Available when **type** is **FWPM_IPSEC_IKEV2_QM_TRANSPORT_CONTEXT**.

### -field ikeV2MmPolicy

Type: **[IKEEXT_POLICY2](../iketypes/ns-iketypes-ikeext_policy2.md)\***

Available when **type** is **FWPM_IPSEC_IKEV2_MM_CONTEXT**.

### -field idpOptions

Type: **[IPSEC_DOSP_OPTIONS0](../ipsectypes/ns-ipsectypes-ipsec_dosp_options0.md)\***

Available when **type** is **FWPM_IPSEC_DOSP_CONTEXT**.

### -field networkConnectionPolicy

A pointer to a [FWPM_NETWORK_CONNECTION_POLICY_SETTINGS0](./ns-fwpmtypes-fwpm_network_connection_policy_setting0.md) structure containing the number of network connection polices, and a list of those policies formatted.

### -field providerContextId

Type: **UINT64**

LUID identifying the context. This is the context value stored in the **FWPS_FILTER1** structure for filters that reference a provider context. The **FWPS_FILTER1** structure is documented in the WDK. This is additional information returned when getting/enumerating objects.

## -remarks

The first seven elements of the union are information supplied when adding objects.

## -see-also

[FWPM_DISPLAY_DATA0](../fwptypes/ns-fwptypes-fwpm_display_data0.md)

[FWPM_PROVIDER_CONTEXT_TYPE](ne-fwpmtypes-fwpm_provider_context_type.md)

[FWP_BYTE_BLOB](../fwptypes/ns-fwptypes-fwp_byte_blob.md)

[FwpmProviderContextAdd2](../fwpmu/nf-fwpmu-fwpmprovidercontextadd2.md)

[IKEEXT_POLICY2](../iketypes/ns-iketypes-ikeext_policy2.md)

[IPSEC_DOSP_OPTIONS0](../ipsectypes/ns-ipsectypes-ipsec_dosp_options0.md)

[IPSEC_KEYING_POLICY0](../ipsectypes/ns-ipsectypes-ipsec_keying_policy0.md)

[IPSEC_TRANSPORT_POLICY2](../ipsectypes/ns-ipsectypes-ipsec_transport_policy2.md)

[IPSEC_TUNNEL_POLICY2](../ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2.md)

[Windows Filtering Platform  API Structures](/windows/desktop/FWP/fwp-structs)
