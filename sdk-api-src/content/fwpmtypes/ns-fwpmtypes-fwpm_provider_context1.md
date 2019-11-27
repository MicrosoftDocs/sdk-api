---
UID: NS:fwpmtypes.FWPM_PROVIDER_CONTEXT1_
title: FWPM_PROVIDER_CONTEXT1 (fwpmtypes.h)

description: Stores the state associated with a provider context.
old-location: fwp\fwpm_provider_context1_struct.htm
tech.root: fwp
ms.assetid: 34727579-9baf-4d50-b973-e864ddf651b0

ms.date: 12/05/2018
ms.keywords: FWPM_PROVIDER_CONTEXT1, FWPM_PROVIDER_CONTEXT1 structure [Filtering], FWPM_PROVIDER_CONTEXT1_, FWPM_PROVIDER_CONTEXT_FLAG_PERSISTENT, fwp.fwpm_provider_context1_struct, fwpmtypes/FWPM_PROVIDER_CONTEXT1
ms.topic: struct
f1_keywords: 
 - "fwpmtypes/FWPM_PROVIDER_CONTEXT1"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_PROVIDER_CONTEXT1
targetos: Windows
req.typenames: FWPM_PROVIDER_CONTEXT1
req.redist: 
ms.custom: 19H1
---

# FWPM_PROVIDER_CONTEXT1 structure


## -description


The <b>FWPM_PROVIDER_CONTEXT1</b> structure stores the state associated with a provider context.
[FWPM_PROVIDER_CONTEXT2](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context2)a> is available. For Windows Vista, [FWPM_PROVIDER_CONTEXT0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context0)a> is available.</div><div> </div>

## -struct-fields




### -field providerContextKey

Uniquely identifies the provider context. If the GUID is zero-initialized
   in the call to <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd1">FwpmProviderContextAdd1</a>, Base Filtering Engine (BFE) will generate one.


### -field displayData

Allows provider contexts to be annotated in a human-readable form. The [FWPM_DISPLAY_DATA0](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwpm_display_data0)a> structure is required.


### -field flags

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
</table>
 


### -field providerKey

GUID of the policy provider that manages this object.


### -field providerData

An [FWP_BYTE_BLOB](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)a> structure that contains optional provider-specific data that allows providers to store additional context info with the object.


### -field type

A [FWPM_PROVIDER_CONTEXT_TYPE](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)a> value specifying the type of provider context..


### -field keyingPolicy

Available when <b>type</b> is <b>FWPM_IPSEC_KEYING_CONTEXT</b>.

See [IPSEC_KEYING_POLICY0](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy0)a> for more information.


### -field ikeQmTransportPolicy

Available when <b>type</b> is <b>FWPM_IPSEC_IKE_QM_TRANSPORT_CONTEXT</b>.

See [IPSEC_TRANSPORT_POLICY1](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy1)a> for more information.


### -field ikeQmTunnelPolicy

Available when <b>type</b> is <b>FWPM_IPSEC_IKE_QM_TUNNEL_CONTEXT</b>.

See [IPSEC_TUNNEL_POLICY1](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy1)a> for more information.


### -field authipQmTransportPolicy

Available when <b>type</b> is <b>FWPM_IPSEC_AUTHIP_QM_TRANSPORT_CONTEXT</b>.

See [IPSEC_TRANSPORT_POLICY1](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy1)a> for more information.


### -field authipQmTunnelPolicy

Available when <b>type</b> is <b>FWPM_IPSEC_AUTHIP_QM_TUNNEL_CONTEXT</b>.

See [IPSEC_TUNNEL_POLICY1](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy1)a> for more information.


### -field ikeMmPolicy

Available when <b>type</b> is <b>FWPM_IPSEC_IKE_MM_CONTEXT</b>.

See [IKEEXT_POLICY1](https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_policy1)a> for more information.


### -field authIpMmPolicy

Available when <b>type</b> is <b>FWPM_IPSEC_AUTHIP_MM_CONTEXT</b>.

See [IKEEXT_POLICY1](https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_policy1)a> for more information.


### -field dataBuffer

Available when <b>type</b> is <b>FWPM_GENERAL_CONTEXT</b>.

See [FWP_BYTE_BLOB](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)a> for more information.


### -field classifyOptions

Available when <b>type</b> is <b>FWPM_CLASSIFY_OPTIONS_CONTEXT</b>.

See [FWPM_CLASSIFY_OPTIONS0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_classify_options0)a> for more information.


### -field ikeV2QmTunnelPolicy

Available when <b>type</b> is <b>FWPM_IPSEC_IKEV2_QM_TUNNEL_CONTEXT</b>.

See [IPSEC_TUNNEL_POLICY1](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy1)a> for more information.


### -field ikeV2MmPolicy

Available when <b>type</b> is <b>FWPM_IPSEC_IKEV2_MM_CONTEXT</b>.

See [IKEEXT_POLICY1](https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_policy1)a> for more information.


### -field idpOptions

Available when <b>type</b> is <b>FWPM_IPSEC_DOSP_CONTEXT</b>.

See [IPSEC_DOSP_OPTIONS0](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_dosp_options0)a> for more information.


### -field providerContextId

LUID identifying the context.  This is the context value stored in the <b>FWPS_FILTER1</b> structure for filters that reference a provider context. The <b>FWPS_FILTER1</b> structure is documented in the WDK.


## -remarks



The first seven elements of the union are information supplied when adding objects.

The last element is additional information returned when getting/enumerating objects.




## -see-also




[FWPM_DISPLAY_DATA0](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwpm_display_data0)a>



[FWPM_PROVIDER_CONTEXT_TYPE](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)a>



[FWP_BYTE_BLOB](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)a>



<a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd1">FwpmProviderContextAdd1</a>



[IKEEXT_POLICY1](https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_policy1)a>



[IPSEC_DOSP_OPTIONS0](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_dosp_options0)a>



[IPSEC_KEYING_POLICY0](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy0)a>



[IPSEC_TRANSPORT_POLICY1](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy1)a>



[IPSEC_TUNNEL_POLICY1](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy1)a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

