---
UID: NS:fwpmtypes.FWPM_NET_EVENT_IKEEXT_MM_FAILURE1_
title: FWPM_NET_EVENT_IKEEXT_MM_FAILURE1 (fwpmtypes.h)
author: windows-sdk-content
description: Contains information that describes an IKE/AuthIP Main Mode (MM) failure.
old-location: fwp\fwpm_net_event_ikeext_mm_failure1.htm
tech.root: fwp
ms.assetid: 4c67353c-289c-42ef-9081-20c33a9a06a4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_IKEEXT_MM_FAILURE1, FWPM_NET_EVENT_IKEEXT_MM_FAILURE1 structure [Filtering], FWPM_NET_EVENT_IKEEXT_MM_FAILURE_FLAG_BENIGN, FWPM_NET_EVENT_IKEEXT_MM_FAILURE_FLAG_MULTIPLE, fwp.fwpm_net_event_ikeext_mm_failure1, fwpmtypes/FWPM_NET_EVENT_IKEEXT_MM_FAILURE1
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
 - FWPM_NET_EVENT_IKEEXT_MM_FAILURE1
product: Windows
targetos: Windows
req.typenames: FWPM_NET_EVENT_IKEEXT_MM_FAILURE1
req.redist: 
ms.custom: 19H1
---

# FWPM_NET_EVENT_IKEEXT_MM_FAILURE1 structure


## -description


The <b>FWPM_NET_EVENT_IKEEXT_MM_FAILURE1</b> structure contains information that describes an IKE/AuthIP Main Mode (MM) failure.
<div class="alert"><b>Note</b>  <b>FWPM_NET_EVENT_IKEEXT_MM_FAILURE1</b> is the specific implementation of FWPM_NET_EVENT_IKEEXT_MM_FAILURE used in Windows Vista. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_mm_failure0_">FWPM_NET_EVENT_IKEEXT_MM_FAILURE0</a> is available.</div><div> </div>

## -struct-fields




### -field failureErrorCode

Windows error code for the failure.


### -field failurePoint

An <a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_failure_point_">IPSEC_FAILURE_POINT</a> value that indicates the IPsec state when the failure occurred.


### -field flags

Flags for the failure event.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_IKEEXT_MM_FAILURE_FLAG_BENIGN"></a><a id="fwpm_net_event_ikeext_mm_failure_flag_benign"></a><dl>
<dt><b>FWPM_NET_EVENT_IKEEXT_MM_FAILURE_FLAG_BENIGN</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the failure was benign or expected.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_IKEEXT_MM_FAILURE_FLAG_MULTIPLE"></a><a id="fwpm_net_event_ikeext_mm_failure_flag_multiple"></a><dl>
<dt><b>FWPM_NET_EVENT_IKEEXT_MM_FAILURE_FLAG_MULTIPLE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that multiple failure events have been reported.

</td>
</tr>
</table>
 


### -field keyingModuleType

 An <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ne-iketypes-ikeext_key_module_type_">IKEEXT_KEY_MODULE_TYPE</a> value that specifies the type of keying module.


### -field mmState

An <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ne-iketypes-ikeext_mm_sa_state_">IKEEXT_MM_SA_STATE</a> value that indicates the Main Mode state when the failure occurred.


### -field saRole

An <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ne-iketypes-ikeext_sa_role_">IKEEXT_SA_ROLE</a> value that specifies the security association (SA) role when the failure occurred.


### -field mmAuthMethod

An <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ne-iketypes-ikeext_authentication_method_type_">IKEEXT_AUTHENTICATION_METHOD_TYPE</a> value that specifies the authentication method.


### -field endCertHash

SHA thumbprint hash of the end certificate corresponding to the failures that happen during building or validating certificate chains.

<b>IKEEXT_CERT_HASH_LEN</b> maps to 20.


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




<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

