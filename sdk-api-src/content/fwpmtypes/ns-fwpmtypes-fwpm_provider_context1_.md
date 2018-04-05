---
UID: NS:fwpmtypes.FWPM_PROVIDER_CONTEXT1_
title: FWPM_PROVIDER_CONTEXT1_
author: windows-driver-content
description: Stores the state associated with a provider context.
old-location: fwp\fwpm_provider_context1_struct.htm
old-project: FWP
ms.assetid: 34727579-9baf-4d50-b973-e864ddf651b0
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: FWPM_PROVIDER_CONTEXT1, FWPM_PROVIDER_CONTEXT1 structure [Filtering], FWPM_PROVIDER_CONTEXT1_, FWPM_PROVIDER_CONTEXT_FLAG_PERSISTENT, fwp.fwpm_provider_context1_struct, fwpmtypes/FWPM_PROVIDER_CONTEXT1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: FWPM_PROVIDER_CONTEXT1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Fwpmtypes.h
api_name:
-	FWPM_PROVIDER_CONTEXT1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FWPM_PROVIDER_CONTEXT1_ structure


## -description


The <b>FWPM_PROVIDER_CONTEXT1</b> structure stores the state associated with a provider context.
<div class="alert"><b>Note</b>  <b>FWPM_PROVIDER_CONTEXT1</b> is the specific implementation of FWPM_PROVIDER_CONTEXT used in Windows 7. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8, <a href="https://msdn.microsoft.com/aa397a4e-07cc-4eee-8d0f-798901a5bb29">FWPM_PROVIDER_CONTEXT2</a> is available. For Windows Vista, <a href="https://msdn.microsoft.com/99105044-f4fa-42f2-8393-f0ee8948e9ff">FWPM_PROVIDER_CONTEXT0</a> is available.</div><div> </div>

## -struct-fields




### -field providerContextKey

Uniquely identifies the provider context. If the GUID is zero-initialized
   in the call to <a href="https://msdn.microsoft.com/2a840f23-96e4-4b3d-b92e-53b3d10ab2bb">FwpmProviderContextAdd1</a>, Base Filtering Engine (BFE) will generate one.


### -field displayData

Allows provider contexts to be annotated in a human-readable form. The <b>name</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550081">FWPM_DISPLAY_DATA0</a> structure is required.


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

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a> structure that contains optional provider-specific data that allows providers to store additional context info with the object.


### -field type

A <a href="https://msdn.microsoft.com/e8eae5e7-9240-47a5-851b-1ec51cb07b63">FWPM_PROVIDER_CONTEXT_TYPE</a> value specifying the type of provider context..


### -field providerContextId

LUID identifying the context.  This is the context value stored in the <b>FWPS_FILTER1</b> structure for filters that reference a provider context. The <b>FWPS_FILTER1</b> structure is documented in the WDK.


#### - authIpMmPolicy

Available when <b>type</b> is <b>FWPM_IPSEC_AUTHIP_MM_CONTEXT</b>.

See <a href="https://msdn.microsoft.com/0834b147-9892-4afe-a5c8-cb782918a868">IKEEXT_POLICY1</a> for more information.


#### - authipQmTransportPolicy

Available when <b>type</b> is <b>FWPM_IPSEC_AUTHIP_QM_TRANSPORT_CONTEXT</b>.

See <a href="https://msdn.microsoft.com/4ee39f30-f7fc-40a9-92b0-e059cb9b84a2">IPSEC_TRANSPORT_POLICY1</a> for more information.


#### - authipQmTunnelPolicy

Available when <b>type</b> is <b>FWPM_IPSEC_AUTHIP_QM_TUNNEL_CONTEXT</b>.

See <a href="https://msdn.microsoft.com/b51d330f-3f10-43e2-9018-eb6fd35ffe25">IPSEC_TUNNEL_POLICY1</a> for more information.


#### - classifyOptions

Available when <b>type</b> is <b>FWPM_CLASSIFY_OPTIONS_CONTEXT</b>.

See <a href="https://msdn.microsoft.com/library/windows/hardware/ff550079">FWPM_CLASSIFY_OPTIONS0</a> for more information.


#### - dataBuffer

Available when <b>type</b> is <b>FWPM_GENERAL_CONTEXT</b>.

See <a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a> for more information.


#### - idpOptions

Available when <b>type</b> is <b>FWPM_IPSEC_DOSP_CONTEXT</b>.

See <a href="https://msdn.microsoft.com/7f180a05-ce8a-4f3b-8e97-d0b6f7f9f8ca">IPSEC_DOSP_OPTIONS0</a> for more information.


#### - ikeMmPolicy

Available when <b>type</b> is <b>FWPM_IPSEC_IKE_MM_CONTEXT</b>.

See <a href="https://msdn.microsoft.com/0834b147-9892-4afe-a5c8-cb782918a868">IKEEXT_POLICY1</a> for more information.


#### - ikeQmTransportPolicy

Available when <b>type</b> is <b>FWPM_IPSEC_IKE_QM_TRANSPORT_CONTEXT</b>.

See <a href="https://msdn.microsoft.com/4ee39f30-f7fc-40a9-92b0-e059cb9b84a2">IPSEC_TRANSPORT_POLICY1</a> for more information.


#### - ikeQmTunnelPolicy

Available when <b>type</b> is <b>FWPM_IPSEC_IKE_QM_TUNNEL_CONTEXT</b>.

See <a href="https://msdn.microsoft.com/b51d330f-3f10-43e2-9018-eb6fd35ffe25">IPSEC_TUNNEL_POLICY1</a> for more information.


#### - ikeV2MmPolicy

Available when <b>type</b> is <b>FWPM_IPSEC_IKEV2_MM_CONTEXT</b>.

See <a href="https://msdn.microsoft.com/0834b147-9892-4afe-a5c8-cb782918a868">IKEEXT_POLICY1</a> for more information.


#### - ikeV2QmTunnelPolicy

Available when <b>type</b> is <b>FWPM_IPSEC_IKEV2_QM_TUNNEL_CONTEXT</b>.

See <a href="https://msdn.microsoft.com/b51d330f-3f10-43e2-9018-eb6fd35ffe25">IPSEC_TUNNEL_POLICY1</a> for more information.


#### - keyingPolicy

Available when <b>type</b> is <b>FWPM_IPSEC_KEYING_CONTEXT</b>.

See <a href="https://msdn.microsoft.com/6eddafbf-ac57-419f-b2a0-f50a4ab31baf">IPSEC_KEYING_POLICY0</a> for more information.


## -remarks



The first seven elements of the union are information supplied when adding objects.

The last element is additional information returned when getting/enumerating objects.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550081">FWPM_DISPLAY_DATA0</a>



<a href="https://msdn.microsoft.com/e8eae5e7-9240-47a5-851b-1ec51cb07b63">FWPM_PROVIDER_CONTEXT_TYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a>



<a href="https://msdn.microsoft.com/2a840f23-96e4-4b3d-b92e-53b3d10ab2bb">FwpmProviderContextAdd1</a>



<a href="https://msdn.microsoft.com/0834b147-9892-4afe-a5c8-cb782918a868">IKEEXT_POLICY1</a>



<a href="https://msdn.microsoft.com/7f180a05-ce8a-4f3b-8e97-d0b6f7f9f8ca">IPSEC_DOSP_OPTIONS0</a>



<a href="https://msdn.microsoft.com/6eddafbf-ac57-419f-b2a0-f50a4ab31baf">IPSEC_KEYING_POLICY0</a>



<a href="https://msdn.microsoft.com/4ee39f30-f7fc-40a9-92b0-e059cb9b84a2">IPSEC_TRANSPORT_POLICY1</a>



<a href="https://msdn.microsoft.com/b51d330f-3f10-43e2-9018-eb6fd35ffe25">IPSEC_TUNNEL_POLICY1</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

