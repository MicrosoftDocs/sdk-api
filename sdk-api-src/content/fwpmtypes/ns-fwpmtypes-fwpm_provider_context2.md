---
UID: NS:fwpmtypes.FWPM_PROVIDER_CONTEXT2_
title: FWPM_PROVIDER_CONTEXT2 (fwpmtypes.h)
description: Stores the state associated with a provider context. (FWPM_PROVIDER_CONTEXT2)
helpviewer_keywords: ["FWPM_PROVIDER_CONTEXT2","FWPM_PROVIDER_CONTEXT2 structure [Filtering]","FWPM_PROVIDER_CONTEXT2_","FWPM_PROVIDER_CONTEXT_FLAG_DOWNLEVEL","FWPM_PROVIDER_CONTEXT_FLAG_PERSISTENT","fwp.fwpm_provider_context2","fwpmtypes/FWPM_PROVIDER_CONTEXT2"]
old-location: fwp\fwpm_provider_context2.htm
tech.root: fwp
ms.assetid: aa397a4e-07cc-4eee-8d0f-798901a5bb29
ms.date: 12/05/2018
ms.keywords: FWPM_PROVIDER_CONTEXT2, FWPM_PROVIDER_CONTEXT2 structure [Filtering], FWPM_PROVIDER_CONTEXT2_, FWPM_PROVIDER_CONTEXT_FLAG_DOWNLEVEL, FWPM_PROVIDER_CONTEXT_FLAG_PERSISTENT, fwp.fwpm_provider_context2, fwpmtypes/FWPM_PROVIDER_CONTEXT2
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
targetos: Windows
req.typenames: FWPM_PROVIDER_CONTEXT2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_PROVIDER_CONTEXT2_
 - fwpmtypes/FWPM_PROVIDER_CONTEXT2_
 - FWPM_PROVIDER_CONTEXT2
 - fwpmtypes/FWPM_PROVIDER_CONTEXT2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fwpmtypes.h
api_name:
 - FWPM_PROVIDER_CONTEXT2
---

## -description

The **FWPM_PROVIDER_CONTEXT2** structure stores the state associated with a provider context. [FWPM_PROVIDER_CONTEXT0](ns-fwpmtypes-fwpm_provider_context0.md) is available.

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

### -field providerContextId

Type: **UINT64**

LUID identifying the context.  This is the context value stored in the **FWPS_FILTER1** structure for filters that reference a provider context. The **FWPS_FILTER1** structure is documented in the WDK.

## -remarks

The first seven elements of the union are information supplied when adding objects.

The last element is additional information returned when getting/enumerating objects.

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
