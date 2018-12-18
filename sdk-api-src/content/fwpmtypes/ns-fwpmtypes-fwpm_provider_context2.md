---
UID: NS:fwpmtypes.FWPM_PROVIDER_CONTEXT2_
title: FWPM_PROVIDER_CONTEXT2
author: windows-sdk-content
description: Stores the state associated with a provider context.
old-location: fwp\fwpm_provider_context2.htm
tech.root: fwp
ms.assetid: aa397a4e-07cc-4eee-8d0f-798901a5bb29
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FWPM_PROVIDER_CONTEXT2, FWPM_PROVIDER_CONTEXT2 structure [Filtering], FWPM_PROVIDER_CONTEXT2_, FWPM_PROVIDER_CONTEXT_FLAG_DOWNLEVEL, FWPM_PROVIDER_CONTEXT_FLAG_PERSISTENT, fwp.fwpm_provider_context2, fwpmtypes/FWPM_PROVIDER_CONTEXT2
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: FWPM_PROVIDER_CONTEXT2
req.redist: 
---

# FWPM_PROVIDER_CONTEXT2 structure


## -description


The <b>FWPM_PROVIDER_CONTEXT2</b> structure stores the state associated with a provider context.
<div class="alert"><b>Note</b>  <b>FWPM_PROVIDER_CONTEXT2</b> is the specific implementation of FWPM_PROVIDER_CONTEXT used in Windows 8. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://msdn.microsoft.com/34727579-9baf-4d50-b973-e864ddf651b0">FWPM_PROVIDER_CONTEXT1</a> is available. For Windows Vista, <a href="https://msdn.microsoft.com/99105044-f4fa-42f2-8393-f0ee8948e9ff">FWPM_PROVIDER_CONTEXT0</a> is available.</div><div> </div>

## -struct-fields




### -field providerContextKey

Type: <b>GUID</b>

Uniquely identifies the provider context. If the GUID is zero-initialized
   in the call to <a href="https://msdn.microsoft.com/07c6b1fc-55bb-4526-a24b-0e22f147e5cc">FwpmProviderContextAdd2</a>, Base Filtering Engine (BFE) will generate one.


### -field displayData

Type: <b><a href="https://msdn.microsoft.com/b86ca572-b4f4-4d40-adfd-fb0e9d32fcd5">FWPM_DISPLAY_DATA0</a></b>

Allows provider contexts to be annotated in a human-readable form. The <b>name</b> member of the <a href="https://msdn.microsoft.com/b86ca572-b4f4-4d40-adfd-fb0e9d32fcd5">FWPM_DISPLAY_DATA0</a> structure is required.


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

Type: <b><a href="https://msdn.microsoft.com/85f360bf-5ee4-4980-b4ce-15ff310d8fbe">FWP_BYTE_BLOB</a></b>

Optional provider-specific data that allows providers to store additional context info with the object.


### -field type

Type: <b><a href="https://msdn.microsoft.com/e8eae5e7-9240-47a5-851b-1ec51cb07b63">FWPM_PROVIDER_CONTEXT_TYPE</a></b>

The type of provider context.


### -field keyingPolicy

Type: <b><a href="https://msdn.microsoft.com/4b574e1c-ce0f-4c72-a14b-5ca0ed8aa005">IPSEC_KEYING_POLICY1</a>*</b>

Available when <b>type</b> is <b>FWPM_IPSEC_KEYING_CONTEXT</b>.


### -field ikeQmTransportPolicy

Type: <b><a href="https://msdn.microsoft.com/fce0ce7e-770c-4cc6-94ea-21af0464f740">IPSEC_TRANSPORT_POLICY2</a>*</b>

Available when <b>type</b> is <b>FWPM_IPSEC_IKE_QM_TRANSPORT_CONTEXT</b>.


### -field ikeQmTunnelPolicy

Type: <b><a href="https://msdn.microsoft.com/a633505d-86ec-42ba-bb4c-3f61e8768eab">IPSEC_TUNNEL_POLICY2</a>*</b>

Available when <b>type</b> is <b>FWPM_IPSEC_IKE_QM_TUNNEL_CONTEXT</b>.


### -field authipQmTransportPolicy

Type: <b><a href="https://msdn.microsoft.com/fce0ce7e-770c-4cc6-94ea-21af0464f740">IPSEC_TRANSPORT_POLICY2</a>*</b>

 [case()][unique] 


### -field authipQmTunnelPolicy

Type: <b><a href="https://msdn.microsoft.com/a633505d-86ec-42ba-bb4c-3f61e8768eab">IPSEC_TUNNEL_POLICY2</a>*</b>

Available when <b>type</b> is <b>FWPM_IPSEC_AUTHIP_QM_TRANSPORT_CONTEXT</b>.


### -field ikeMmPolicy

Type: <b><a href="https://msdn.microsoft.com/d6efc1dd-3127-44d0-9f6a-ebf7cba477aa">IKEEXT_POLICY2</a>*</b>

Available when <b>type</b> is <b>FWPM_IPSEC_IKE_MM_CONTEXT</b>.


### -field authIpMmPolicy

Type: <b><a href="https://msdn.microsoft.com/d6efc1dd-3127-44d0-9f6a-ebf7cba477aa">IKEEXT_POLICY2</a>*</b>

Available when <b>type</b> is <b>FWPM_IPSEC_AUTHIP_MM_CONTEXT</b>.


### -field dataBuffer

Type: <b><a href="https://msdn.microsoft.com/85f360bf-5ee4-4980-b4ce-15ff310d8fbe">FWP_BYTE_BLOB</a>*</b>

Available when <b>type</b> is <b>FWPM_GENERAL_CONTEXT</b>.


### -field classifyOptions

Type: <b><a href="https://msdn.microsoft.com/5d1f7807-4188-4a57-83fc-99683254e3a5">FWPM_CLASSIFY_OPTIONS0</a>*</b>

Available when <b>type</b> is <b>FWPM_CLASSIFY_OPTIONS_CONTEXT</b>.


### -field ikeV2QmTunnelPolicy

Type: <b><a href="https://msdn.microsoft.com/a633505d-86ec-42ba-bb4c-3f61e8768eab">IPSEC_TUNNEL_POLICY2</a>*</b>

Available when <b>type</b> is <b>FWPM_IPSEC_IKEV2_QM_TUNNEL_CONTEXT</b>.


### -field ikeV2QmTransportPolicy

Type: <b><a href="https://msdn.microsoft.com/fce0ce7e-770c-4cc6-94ea-21af0464f740">IPSEC_TRANSPORT_POLICY2</a>*</b>

Available when <b>type</b> is <b>FWPM_IPSEC_IKEV2_QM_TRANSPORT_CONTEXT</b>.


### -field ikeV2MmPolicy

Type: <b><a href="https://msdn.microsoft.com/d6efc1dd-3127-44d0-9f6a-ebf7cba477aa">IKEEXT_POLICY2</a>*</b>

Available when <b>type</b> is <b>FWPM_IPSEC_IKEV2_MM_CONTEXT</b>.


### -field idpOptions

Type: <b><a href="https://msdn.microsoft.com/7f180a05-ce8a-4f3b-8e97-d0b6f7f9f8ca">IPSEC_DOSP_OPTIONS0</a>*</b>

Available when <b>type</b> is <b>FWPM_IPSEC_DOSP_CONTEXT</b>.


### -field providerContextId

Type: <b>UINT64</b>

LUID identifying the context.  This is the context value stored in the <b>FWPS_FILTER1</b> structure for filters that reference a provider context. The <b>FWPS_FILTER1</b> structure is documented in the WDK.


## -remarks



The first seven elements of the union are information supplied when adding objects.

The last element is additional information returned when getting/enumerating objects.




## -see-also




<a href="https://msdn.microsoft.com/b86ca572-b4f4-4d40-adfd-fb0e9d32fcd5">FWPM_DISPLAY_DATA0</a>



<a href="https://msdn.microsoft.com/e8eae5e7-9240-47a5-851b-1ec51cb07b63">FWPM_PROVIDER_CONTEXT_TYPE</a>



<a href="https://msdn.microsoft.com/85f360bf-5ee4-4980-b4ce-15ff310d8fbe">FWP_BYTE_BLOB</a>



<a href="https://msdn.microsoft.com/07c6b1fc-55bb-4526-a24b-0e22f147e5cc">FwpmProviderContextAdd2</a>



<a href="https://msdn.microsoft.com/d6efc1dd-3127-44d0-9f6a-ebf7cba477aa">IKEEXT_POLICY2</a>



<a href="https://msdn.microsoft.com/7f180a05-ce8a-4f3b-8e97-d0b6f7f9f8ca">IPSEC_DOSP_OPTIONS0</a>



<a href="https://msdn.microsoft.com/6eddafbf-ac57-419f-b2a0-f50a4ab31baf">IPSEC_KEYING_POLICY0</a>



<a href="https://msdn.microsoft.com/fce0ce7e-770c-4cc6-94ea-21af0464f740">IPSEC_TRANSPORT_POLICY2</a>



<a href="https://msdn.microsoft.com/a633505d-86ec-42ba-bb4c-3f61e8768eab">IPSEC_TUNNEL_POLICY2</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

