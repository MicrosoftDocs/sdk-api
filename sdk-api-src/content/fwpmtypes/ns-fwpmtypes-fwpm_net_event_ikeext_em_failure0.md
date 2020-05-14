---
UID: NS:fwpmtypes.FWPM_NET_EVENT_IKEEXT_EM_FAILURE0_
title: FWPM_NET_EVENT_IKEEXT_EM_FAILURE0 (fwpmtypes.h)
description: The FWPM_NET_EVENT_IKEEXT_EM_FAILURE0 structure contains information that describes an IKE Extended Mode (EM) failure.Note  FWPM_NET_EVENT_IKEEXT_EM_FAILURE0 is the specific implementation of FWPM_NET_EVENT_IKEEXT_EM_FAILURE used in Windows Vista.
helpviewer_keywords: ["FWPM_NET_EVENT_IKEEXT_EM_FAILURE0","FWPM_NET_EVENT_IKEEXT_EM_FAILURE0 structure [Filtering]","FWPM_NET_EVENT_IKEEXT_EM_FAILURE_FLAG_MULTIPLE","fwp.fwpm_net_event_ikeext_em_failure0","fwpmtypes/FWPM_NET_EVENT_IKEEXT_EM_FAILURE0"]
old-location: fwp\fwpm_net_event_ikeext_em_failure0.htm
tech.root: fwp
ms.assetid: 53b28166-8f19-4891-aeb0-603628d95053
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_IKEEXT_EM_FAILURE0, FWPM_NET_EVENT_IKEEXT_EM_FAILURE0 structure [Filtering], FWPM_NET_EVENT_IKEEXT_EM_FAILURE_FLAG_MULTIPLE, fwp.fwpm_net_event_ikeext_em_failure0, fwpmtypes/FWPM_NET_EVENT_IKEEXT_EM_FAILURE0
f1_keywords:
- fwpmtypes/FWPM_NET_EVENT_IKEEXT_EM_FAILURE0
dev_langs:
- c++
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
- FWPM_NET_EVENT_IKEEXT_EM_FAILURE0
targetos: Windows
req.typenames: FWPM_NET_EVENT_IKEEXT_EM_FAILURE0
req.redist: 
ms.custom: 19H1
---

# FWPM_NET_EVENT_IKEEXT_EM_FAILURE0 structure


## -description


The <b>FWPM_NET_EVENT_IKEEXT_EM_FAILURE0</b> structure contains information that describes an IKE Extended Mode (EM) failure.
[FWPM_NET_EVENT_IKEEXT_EM_FAILURE1](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_em_failure1) is available.</div><div> </div>

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


## -see-also




<a href="/windows/win32/api/iketypes/ne-iketypes-ikeext_authentication_method_type">IKEEXT_AUTHENTICATION_METHOD_TYPE</a>



[IKEEXT_EM_SA_STATE](https://docs.microsoft.com/windows/desktop/api/iketypes/ne-iketypes-ikeext_em_sa_state)



[IKEEXT_SA_ROLE](https://docs.microsoft.com/windows/desktop/api/iketypes/ne-iketypes-ikeext_sa_role)



[IPSEC_FAILURE_POINT](https://docs.microsoft.com/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_failure_point)



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

