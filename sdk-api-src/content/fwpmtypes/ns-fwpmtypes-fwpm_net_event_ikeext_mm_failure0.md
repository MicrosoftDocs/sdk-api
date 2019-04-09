---
UID: NS:fwpmtypes.FWPM_NET_EVENT_IKEEXT_MM_FAILURE0_
title: FWPM_NET_EVENT_IKEEXT_MM_FAILURE0 (fwpmtypes.h)
author: windows-sdk-content
description: Contains information that describes an IKE/AuthIP Main Mode (MM) failure.
old-location: fwp\fwpm_net_event_ikeext_mm_failure0.htm
tech.root: fwp
ms.assetid: 66845a68-e465-44d9-afc0-3d95b10cc69f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_IKEEXT_MM_FAILURE0, FWPM_NET_EVENT_IKEEXT_MM_FAILURE0 structure [Filtering], FWPM_NET_EVENT_IKEEXT_MM_FAILURE_FLAG_BENIGN, FWPM_NET_EVENT_IKEEXT_MM_FAILURE_FLAG_MULTIPLE, fwp.fwpm_net_event_ikeext_mm_failure0, fwpmtypes/FWPM_NET_EVENT_IKEEXT_MM_FAILURE0
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
 - FWPM_NET_EVENT_IKEEXT_MM_FAILURE0
product: Windows
targetos: Windows
req.typenames: FWPM_NET_EVENT_IKEEXT_MM_FAILURE0
req.redist: 
---

# FWPM_NET_EVENT_IKEEXT_MM_FAILURE0 structure


## -description


The <b>FWPM_NET_EVENT_IKEEXT_MM_FAILURE0</b> structure contains information that describes an IKE/AuthIP Main Mode (MM) failure.
<div class="alert"><b>Note</b>  <b>FWPM_NET_EVENT_IKEEXT_MM_FAILURE0</b> is the specific implementation of FWPM_NET_EVENT_IKEEXT_MM_FAILURE used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://msdn.microsoft.com/en-us/library/Ee707313(v=VS.85).aspx">FWPM_NET_EVENT_IKEEXT_MM_FAILURE1</a> is available.</div><div> </div>

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

 An <a href="https://msdn.microsoft.com/a9268b07-343a-4a51-bc70-3e624facf617">IKEEXT_KEY_MODULE_TYPE</a> value that specifies the type of keying module.


### -field mmState

An <a href="https://msdn.microsoft.com/5af48053-23b7-489f-82b7-743153aea641">IKEEXT_MM_SA_STATE</a> value that indicates the Main Mode state when the failure occurred.


### -field saRole

An <a href="https://msdn.microsoft.com/6bb1e264-6141-4545-add5-e12f09769e25">IKEEXT_SA_ROLE</a> value that specifies the security association (SA) role when the failure occurred.


### -field mmAuthMethod

An <a href="https://msdn.microsoft.com/en-us/library/Aa364977(v=VS.85).aspx">IKEEXT_AUTHENTICATION_METHOD_TYPE</a> value that specifies the authentication method.


### -field endCertHash

SHA thumbprint hash of the end certificate corresponding to the failures that happen during building or validating certificate chains.

<b>IKEEXT_CERT_HASH_LEN</b> maps to 20.


### -field mmId

LUID for the MM SA.


### -field mmFilterId

Main mode filter ID.


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

