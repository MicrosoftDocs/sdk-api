---
UID: NS:fwpmtypes.FWPM_NET_EVENT_IKEEXT_EM_FAILURE1_
title: FWPM_NET_EVENT_IKEEXT_EM_FAILURE1 (fwpmtypes.h)
description: The FWPM_NET_EVENT_IKEEXT_EM_FAILURE1 structure contains information that describes an IKE Extended mode (EM) failure.Note  FWPM_NET_EVENT_IKEEXT_EM_FAILURE1 is the specific implementation of FWPM_NET_EVENT_IKEEXT_EM_FAILURE used in Windows 7 and later.
helpviewer_keywords: ["FWPM_NET_EVENT_IKEEXT_EM_FAILURE1","FWPM_NET_EVENT_IKEEXT_EM_FAILURE1 structure [Filtering]","FWPM_NET_EVENT_IKEEXT_EM_FAILURE_FLAG_BENIGN","FWPM_NET_EVENT_IKEEXT_EM_FAILURE_FLAG_MULTIPLE","fwp.fwpm_net_event_ikeext_em_failure1","fwpmtypes/FWPM_NET_EVENT_IKEEXT_EM_FAILURE1"]
old-location: fwp\fwpm_net_event_ikeext_em_failure1.htm
tech.root: fwp
ms.assetid: 42348e1d-e3b3-4f8c-9fef-15e2e4ebf580
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_IKEEXT_EM_FAILURE1, FWPM_NET_EVENT_IKEEXT_EM_FAILURE1 structure [Filtering], FWPM_NET_EVENT_IKEEXT_EM_FAILURE_FLAG_BENIGN, FWPM_NET_EVENT_IKEEXT_EM_FAILURE_FLAG_MULTIPLE, fwp.fwpm_net_event_ikeext_em_failure1, fwpmtypes/FWPM_NET_EVENT_IKEEXT_EM_FAILURE1
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
req.typenames: FWPM_NET_EVENT_IKEEXT_EM_FAILURE1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_NET_EVENT_IKEEXT_EM_FAILURE1_
 - fwpmtypes/FWPM_NET_EVENT_IKEEXT_EM_FAILURE1_
 - FWPM_NET_EVENT_IKEEXT_EM_FAILURE1
 - fwpmtypes/FWPM_NET_EVENT_IKEEXT_EM_FAILURE1
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
 - FWPM_NET_EVENT_IKEEXT_EM_FAILURE1
---

# FWPM_NET_EVENT_IKEEXT_EM_FAILURE1 structure


## -description

The <b>FWPM_NET_EVENT_IKEEXT_EM_FAILURE1</b> structure contains information that describes an IKE Extended mode (EM) failure.
[FWPM_NET_EVENT_IKEEXT_EM_FAILURE0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_em_failure0) is available.</div><div> </div>

## -struct-fields

### -field failureErrorCode

Windows error code for the failure.

### -field failurePoint

An [IPSEC_FAILURE_POINT](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_failure_point) value that indicates the IPsec state when the failure occurred.

### -field flags

Flags for the failure event.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_IKEEXT_EM_FAILURE_FLAG_MULTIPLE"></a><a id="fwpm_net_event_ikeext_em_failure_flag_multiple"></a><dl>
<dt><b>FWPM_NET_EVENT_IKEEXT_EM_FAILURE_FLAG_MULTIPLE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that multiple IKE EM failure events have been reported.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_IKEEXT_EM_FAILURE_FLAG_BENIGN"></a><a id="fwpm_net_event_ikeext_em_failure_flag_benign"></a><dl>
<dt><b>FWPM_NET_EVENT_IKEEXT_EM_FAILURE_FLAG_BENIGN</b></dt>
</dl>
</td>
<td width="60%">
Indicates that IKE EM failure events have been reported, but that the events are benign. 

</td>
</tr>
</table>

### -field emState

An [IKEEXT_EM_SA_STATE](https://docs.microsoft.com/windows/desktop/api/iketypes/ne-iketypes-ikeext_em_sa_state) value that indicates the EM state when the failure occurred.

### -field saRole

An [IKEEXT_SA_ROLE](https://docs.microsoft.com/windows/desktop/api/iketypes/ne-iketypes-ikeext_sa_role) value that specifies the SA role when the failure occurred.

### -field emAuthMethod

An <a href="/windows/win32/api/iketypes/ne-iketypes-ikeext_authentication_method_type">IKEEXT_AUTHENTICATION_METHOD_TYPE</a> value that specifies the authentication method.

### -field endCertHash

SHA thumbprint hash of the end certificate corresponding to the failures that happen during building or validating certificate chains.

<b>IKEEXT_CERT_HASH_LEN</b> maps to 20.

### -field mmId

LUID for the Main Mode (MM) SA.

### -field qmFilterId

Quick Mode (QM) filter ID associated with this failure.

### -field localPrincipalNameForAuth

Name of the EM local security principal.

### -field remotePrincipalNameForAuth

Name of the EM remote security principal.

### -field numLocalPrincipalGroupSids

Number of groups in the local security principal's token.

### -field localPrincipalGroupSids

Groups in the local security principal's token.

### -field numRemotePrincipalGroupSids

Number of groups in the remote security principal's token.

### -field remotePrincipalGroupSids

Groups in the remote security principal's token.

### -field saTrafficType

Type of traffic for which the embedded quick mode was being negotiated.

## -see-also

<a href="/windows/win32/api/iketypes/ne-iketypes-ikeext_authentication_method_type">IKEEXT_AUTHENTICATION_METHOD_TYPE</a>



[IKEEXT_EM_SA_STATE](https://docs.microsoft.com/windows/desktop/api/iketypes/ne-iketypes-ikeext_em_sa_state)



[IKEEXT_SA_ROLE](https://docs.microsoft.com/windows/desktop/api/iketypes/ne-iketypes-ikeext_sa_role)



[IPSEC_FAILURE_POINT](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_failure_point)



[IPSEC_TRAFFIC_TYPE](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_traffic_type)



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>

