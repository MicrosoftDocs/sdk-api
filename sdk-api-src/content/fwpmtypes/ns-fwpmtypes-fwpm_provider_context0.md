---
UID: NS:fwpmtypes.FWPM_PROVIDER_CONTEXT0_
title: FWPM_PROVIDER_CONTEXT0 (fwpmtypes.h)
description: Stores the state associated with a provider context. (FWPM_PROVIDER_CONTEXT0)
helpviewer_keywords: ["FWPM_PROVIDER_CONTEXT0","FWPM_PROVIDER_CONTEXT0 structure [Filtering]","FWPM_PROVIDER_CONTEXT0_","FWPM_PROVIDER_CONTEXT_FLAG_PERSISTENT","fwp.fwpm_provider_context0_struct","fwpmtypes/FWPM_PROVIDER_CONTEXT0"]
old-location: fwp\fwpm_provider_context0_struct.htm
tech.root: fwp
ms.assetid: 99105044-f4fa-42f2-8393-f0ee8948e9ff
ms.date: 12/05/2018
ms.keywords: FWPM_PROVIDER_CONTEXT0, FWPM_PROVIDER_CONTEXT0 structure [Filtering], FWPM_PROVIDER_CONTEXT0_, FWPM_PROVIDER_CONTEXT_FLAG_PERSISTENT, fwp.fwpm_provider_context0_struct, fwpmtypes/FWPM_PROVIDER_CONTEXT0
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWPM_PROVIDER_CONTEXT0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_PROVIDER_CONTEXT0_
 - fwpmtypes/FWPM_PROVIDER_CONTEXT0_
 - FWPM_PROVIDER_CONTEXT0
 - fwpmtypes/FWPM_PROVIDER_CONTEXT0
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
 - FWPM_PROVIDER_CONTEXT0
---

# FWPM_PROVIDER_CONTEXT0 structure


## -description

The **FWPM_PROVIDER_CONTEXT0** structure stores the state associated with a provider context.
[FWPM_PROVIDER_CONTEXT2](ns-fwpmtypes-fwpm_provider_context2.md) is available.

## -struct-fields

### -field providerContextKey

Uniquely identifies the provider context. If the GUID is zero-initialized in the call to [FwpmProviderContextAdd0](../fwpmu/nf-fwpmu-fwpmprovidercontextadd0.md), Base Filtering Engine (BFE) will generate one.

### -field displayData

Allows provider contexts to be annotated in a human-readable form. The [FWPM_DISPLAY_DATA0](../fwptypes/ns-fwptypes-fwpm_display_data0.md) structure is required.

### -field flags

Possible values:

| Provider context flag | Meaning |
| ----- | ------- |
| FWPM_PROVIDER_CONTEXT_FLAG_PERSISTENT | The object is persistent, that is, it survives across BFE stop/start. |

### -field providerKey

GUID of the policy provider that manages this object.

### -field providerData

An [FWP_BYTE_BLOB](../fwptypes/ns-fwptypes-fwp_byte_blob.md) structure that contains optional provider-specific data that allows providers to store additional context info with the object.

### -field type

A [FWPM_PROVIDER_CONTEXT_TYPE](ne-fwpmtypes-fwpm_provider_context_type.md) value specifying the type of provider context..

### -field keyingPolicy

Available when **type** is **FWPM_IPSEC_KEYING_CONTEXT**.

See [IPSEC_KEYING_POLICY0](../ipsectypes/ns-ipsectypes-ipsec_keying_policy0.md) for more information.

### -field ikeQmTransportPolicy

Available when **type** is **FWPM_IPSEC_IKE_QM_TRANSPORT_CONTEXT**.

See [IPSEC_TRANSPORT_POLICY0](../ipsectypes/ns-ipsectypes-ipsec_transport_policy0.md) for more information.

### -field ikeQmTunnelPolicy

Available when **type** is **FWPM_IPSEC_IKE_QM_TUNNEL_CONTEXT**.

See [IPSEC_TUNNEL_POLICY0](../ipsectypes/ns-ipsectypes-ipsec_tunnel_policy0.md) for more information.

### -field authipQmTransportPolicy

Available when **type** is **FWPM_IPSEC_AUTHIP_QM_TRANSPORT_CONTEXT**.

See [IPSEC_TRANSPORT_POLICY0](../ipsectypes/ns-ipsectypes-ipsec_transport_policy0.md) for more information.

### -field authipQmTunnelPolicy

Available when **type** is **FWPM_IPSEC_AUTHIP_QM_TUNNEL_CONTEXT**.

See [IPSEC_TUNNEL_POLICY0](../ipsectypes/ns-ipsectypes-ipsec_tunnel_policy0.md) for more information.

### -field ikeMmPolicy

Available when **type** is **FWPM_IPSEC_IKE_MM_CONTEXT**.

See [IKEEXT_POLICY0](../iketypes/ns-iketypes-ikeext_policy0.md) for more information.

### -field authIpMmPolicy

Available when **type** is **FWPM_IPSEC_AUTHIP_MM_CONTEXT**.

See [IKEEXT_POLICY0](../iketypes/ns-iketypes-ikeext_policy0.md) for more information.

### -field dataBuffer

Available when **type** is **FWPM_GENERAL_CONTEXT**.

See [FWP_BYTE_BLOB](../fwptypes/ns-fwptypes-fwp_byte_blob.md) for more information.

### -field classifyOptions

Available when **type** is **FWPM_CLASSIFY_OPTIONS_CONTEXT**.

See [FWPM_CLASSIFY_OPTIONS0](ns-fwpmtypes-fwpm_classify_options0.md) for more information.

### -field providerContextId

LUID identifying the context.  This is the context value stored in the **FWPS_FILTER0** structure for filters that reference a provider context. The **FWPS_FILTER0** structure is documented in the WDK.

## -remarks

The first seven elements of the union are information supplied when adding objects.

The last element is additional information returned when getting/enumerating objects.

## -see-also

[Windows Filtering Platform  API Structures](/windows/desktop/FWP/fwp-structs)
