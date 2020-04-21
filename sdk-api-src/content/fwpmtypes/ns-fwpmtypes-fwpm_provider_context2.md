---
UID: NS:fwpmtypes.FWPM_PROVIDER_CONTEXT2_
title: FWPM_PROVIDER_CONTEXT2 (fwpmtypes.h)
description: Stores the state associated with a provider context.helpviewer_keywords: ["FWPM_PROVIDER_CONTEXT2","FWPM_PROVIDER_CONTEXT2 structure [Filtering]","FWPM_PROVIDER_CONTEXT2_","FWPM_PROVIDER_CONTEXT_FLAG_DOWNLEVEL","FWPM_PROVIDER_CONTEXT_FLAG_PERSISTENT","fwp.fwpm_provider_context2","fwpmtypes/FWPM_PROVIDER_CONTEXT2"]
old-location: fwp\fwpm_provider_context2.htm
tech.root: fwp
ms.assetid: aa397a4e-07cc-4eee-8d0f-798901a5bb29
ms.date: 12/05/2018
ms.keywords: FWPM_PROVIDER_CONTEXT2, FWPM_PROVIDER_CONTEXT2 structure [Filtering], FWPM_PROVIDER_CONTEXT2_, FWPM_PROVIDER_CONTEXT_FLAG_DOWNLEVEL, FWPM_PROVIDER_CONTEXT_FLAG_PERSISTENT, fwp.fwpm_provider_context2, fwpmtypes/FWPM_PROVIDER_CONTEXT2
f1_keywords:
- fwpmtypes/FWPM_PROVIDER_CONTEXT2
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
- fwpmtypes.h
api_name:
- FWPM_PROVIDER_CONTEXT2
targetos: Windows
req.typenames: FWPM_PROVIDER_CONTEXT2
req.redist: 
ms.custom: 19H1
---

# FWPM_PROVIDER_CONTEXT2 structure


## -description


The <b>FWPM_PROVIDER_CONTEXT2</b> structure stores the state associated with a provider context.
[FWPM_PROVIDER_CONTEXT0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context0)a> is available.</div><div> </div>

## -struct-fields




### -field providerContextKey

Type: <b>GUID</b>

Uniquely identifies the provider context. If the GUID is zero-initialized
   in the call to <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd2">FwpmProviderContextAdd2</a>, Base Filtering Engine (BFE) will generate one.


### -field displayData

Type: [FWPM_DISPLAY_DATA0](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwpm_display_data0)a></b>

Allows provider contexts to be annotated in a human-readable form. The [FWPM_DISPLAY_DATA0](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwpm_display_data0)a> structure is required.


### -field flags

Type: <b>UINT32</b>

Possible values:

<table>
<tr>
<th>Provider context flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FWPM_PROVIDER_CONTEXT_FLAG_PERSISTENT"></a><a id="fwpm_provider_context_flag_persistent"></a><dl>
<dt><b>FWPM_PROVIDER_CONTEXT_FLAG_PERSISTENT</b></dt>
</dl>
</td>
<td width="60%">
The object is persistent, that is, it survives across BFE stop/start.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_PROVIDER_CONTEXT_FLAG_DOWNLEVEL"></a><a id="fwpm_provider_context_flag_downlevel"></a><dl>
<dt><b>FWPM_PROVIDER_CONTEXT_FLAG_DOWNLEVEL</b></dt>
</dl>
</td>
<td width="60%">
Reserved for internal use.

</td>
</tr>
</table>
 


### -field providerKey

Type: <b>GUID*</b>

GUID of the policy provider that manages this object.


### -field providerData

Type: [FWP_BYTE_BLOB](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)a></b>

Optional provider-specific data that allows providers to store additional context info with the object.


### -field type

Type: [FWPM_PROVIDER_CONTEXT_TYPE](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)a></b>

The type of provider context.


### -field keyingPolicy

Type: [IPSEC_KEYING_POLICY1](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1)a>*</b>

Available when <b>type</b> is <b>FWPM_IPSEC_KEYING_CONTEXT</b>.


### -field ikeQmTransportPolicy

Type: [IPSEC_TRANSPORT_POLICY2](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)a>*</b>

Available when <b>type</b> is <b>FWPM_IPSEC_IKE_QM_TRANSPORT_CONTEXT</b>.


### -field ikeQmTunnelPolicy

Type: [IPSEC_TUNNEL_POLICY2](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)a>*</b>

Available when <b>type</b> is <b>FWPM_IPSEC_IKE_QM_TUNNEL_CONTEXT</b>.


### -field authipQmTransportPolicy

Type: [IPSEC_TRANSPORT_POLICY2](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)a>*</b>

 [case()][unique] 


### -field authipQmTunnelPolicy

Type: [IPSEC_TUNNEL_POLICY2](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)a>*</b>

Available when <b>type</b> is <b>FWPM_IPSEC_AUTHIP_QM_TRANSPORT_CONTEXT</b>.


### -field ikeMmPolicy

Type: [IKEEXT_POLICY2](https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_policy2)a>*</b>

Available when <b>type</b> is <b>FWPM_IPSEC_IKE_MM_CONTEXT</b>.


### -field authIpMmPolicy

Type: [IKEEXT_POLICY2](https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_policy2)a>*</b>

Available when <b>type</b> is <b>FWPM_IPSEC_AUTHIP_MM_CONTEXT</b>.


### -field dataBuffer

Type: [FWP_BYTE_BLOB](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)a>*</b>

Available when <b>type</b> is <b>FWPM_GENERAL_CONTEXT</b>.


### -field classifyOptions

Type: [FWPM_CLASSIFY_OPTIONS0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_classify_options0)a>*</b>

Available when <b>type</b> is <b>FWPM_CLASSIFY_OPTIONS_CONTEXT</b>.


### -field ikeV2QmTunnelPolicy

Type: [IPSEC_TUNNEL_POLICY2](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)a>*</b>

Available when <b>type</b> is <b>FWPM_IPSEC_IKEV2_QM_TUNNEL_CONTEXT</b>.


### -field ikeV2QmTransportPolicy

Type: [IPSEC_TRANSPORT_POLICY2](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)a>*</b>

Available when <b>type</b> is <b>FWPM_IPSEC_IKEV2_QM_TRANSPORT_CONTEXT</b>.


### -field ikeV2MmPolicy

Type: [IKEEXT_POLICY2](https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_policy2)a>*</b>

Available when <b>type</b> is <b>FWPM_IPSEC_IKEV2_MM_CONTEXT</b>.


### -field idpOptions

Type: [IPSEC_DOSP_OPTIONS0](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_dosp_options0)a>*</b>

Available when <b>type</b> is <b>FWPM_IPSEC_DOSP_CONTEXT</b>.


### -field providerContextId

Type: <b>UINT64</b>

LUID identifying the context.  This is the context value stored in the <b>FWPS_FILTER1</b> structure for filters that reference a provider context. The <b>FWPS_FILTER1</b> structure is documented in the WDK.


## -remarks



The first seven elements of the union are information supplied when adding objects.

The last element is additional information returned when getting/enumerating objects.




## -see-also




[FWPM_DISPLAY_DATA0](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwpm_display_data0)a>



[FWPM_PROVIDER_CONTEXT_TYPE](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)a>



[FWP_BYTE_BLOB](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)a>



<a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd2">FwpmProviderContextAdd2</a>



[IKEEXT_POLICY2](https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_policy2)a>



[IPSEC_DOSP_OPTIONS0](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_dosp_options0)a>



[IPSEC_KEYING_POLICY0](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy0)a>



[IPSEC_TRANSPORT_POLICY2](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)a>



[IPSEC_TUNNEL_POLICY2](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

