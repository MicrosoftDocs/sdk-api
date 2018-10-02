---
UID: NS:fwpmtypes.FWPM_NET_EVENT_IKEEXT_EM_FAILURE0_
title: FWPM_NET_EVENT_IKEEXT_EM_FAILURE0_
author: windows-sdk-content
description: The FWPM_NET_EVENT_IKEEXT_EM_FAILURE0 structure contains information that describes an IKE Extended Mode (EM) failure.Note  FWPM_NET_EVENT_IKEEXT_EM_FAILURE0 is the specific implementation of FWPM_NET_EVENT_IKEEXT_EM_FAILURE used in Windows Vista.
old-location: fwp\fwpm_net_event_ikeext_em_failure0.htm
tech.root: FWP
ms.assetid: 53b28166-8f19-4891-aeb0-603628d95053
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FWPM_NET_EVENT_IKEEXT_EM_FAILURE0, FWPM_NET_EVENT_IKEEXT_EM_FAILURE0 structure [Filtering], FWPM_NET_EVENT_IKEEXT_EM_FAILURE0_, FWPM_NET_EVENT_IKEEXT_EM_FAILURE_FLAG_MULTIPLE, fwp.fwpm_net_event_ikeext_em_failure0, fwpmtypes/FWPM_NET_EVENT_IKEEXT_EM_FAILURE0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: FWPM_NET_EVENT_IKEEXT_EM_FAILURE0
req.redist: 
---

# FWPM_NET_EVENT_IKEEXT_EM_FAILURE0_ structure


## -description


The <b>FWPM_NET_EVENT_IKEEXT_EM_FAILURE0</b> structure contains information that describes an IKE Extended Mode (EM) failure.
<div class="alert"><b>Note</b>  <b>FWPM_NET_EVENT_IKEEXT_EM_FAILURE0</b> is the specific implementation of FWPM_NET_EVENT_IKEEXT_EM_FAILURE used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://msdn.microsoft.com/42348e1d-e3b3-4f8c-9fef-15e2e4ebf580">FWPM_NET_EVENT_IKEEXT_EM_FAILURE1</a> is available.</div><div> </div>

## -struct-fields




### -field failureErrorCode

Windows error code for the failure.


### -field failurePoint

An <a href="https://msdn.microsoft.com/750a5643-1157-4d15-9564-127756cd08cd">IPSEC_FAILURE_POINT</a> value that indicates the IPsec state when the failure occurred.


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

An <a href="https://msdn.microsoft.com/378b4a24-4a31-4e9e-83f2-aec9266d1a94">IKEEXT_EM_SA_STATE</a> value that indicates the EM state when the failure occurred.


### -field saRole

An <a href="https://msdn.microsoft.com/6bb1e264-6141-4545-add5-e12f09769e25">IKEEXT_SA_ROLE</a> value that specifies the SA role when the failure occurred.


### -field emAuthMethod

An <a href="https://msdn.microsoft.com/582ec1ea-9390-4f86-9a3c-25d4e805a218">IKEEXT_AUTHENTICATION_METHOD_TYPE</a> value that specifies the authentication method.


### -field endCertHash

SHA thumbprint hash of the end certificate corresponding to the failures that happen during building or validating certificate chains.

<b>IKEEXT_CERT_HASH_LEN</b> maps to 20.


### -field mmId

LUID for the Main Mode (MM) SA.


### -field qmFilterId

Quick Mode (QM) filter ID associated with this failure.


## -see-also




<a href="https://msdn.microsoft.com/582ec1ea-9390-4f86-9a3c-25d4e805a218">IKEEXT_AUTHENTICATION_METHOD_TYPE</a>



<a href="https://msdn.microsoft.com/378b4a24-4a31-4e9e-83f2-aec9266d1a94">IKEEXT_EM_SA_STATE</a>



<a href="https://msdn.microsoft.com/6bb1e264-6141-4545-add5-e12f09769e25">IKEEXT_SA_ROLE</a>



<a href="https://msdn.microsoft.com/750a5643-1157-4d15-9564-127756cd08cd">IPSEC_FAILURE_POINT</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

