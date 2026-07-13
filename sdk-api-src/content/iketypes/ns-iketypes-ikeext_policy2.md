---
UID: NS:iketypes.IKEEXT_POLICY2_
title: IKEEXT_POLICY2 (iketypes.h)
description: Is used to store the IKE/AuthIP main mode negotiation policy. (IKEEXT_POLICY2)
helpviewer_keywords: ["IKEEXT_POLICY2","IKEEXT_POLICY2 structure [Filtering]","IKEEXT_POLICY_FLAG_DISABLE_DIAGNOSTICS","IKEEXT_POLICY_FLAG_ENABLE_OPTIONAL_DH","IKEEXT_POLICY_FLAG_NO_IMPERSONATION_LUID_VERIFY","IKEEXT_POLICY_FLAG_NO_MACHINE_LUID_VERIFY","fwp.ikeext_policy2","iketypes/IKEEXT_POLICY2","IKEEXT_POLICY_FLAG_POINT_TO_SITE"]
old-location: fwp\ikeext_policy2.htm
tech.root: fwp
ms.assetid: d6efc1dd-3127-44d0-9f6a-ebf7cba477aa
ms.date: 12/05/2018
ms.keywords: IKEEXT_POLICY2, IKEEXT_POLICY2 structure [Filtering], IKEEXT_POLICY_FLAG_DISABLE_DIAGNOSTICS, IKEEXT_POLICY_FLAG_ENABLE_OPTIONAL_DH, IKEEXT_POLICY_FLAG_NO_IMPERSONATION_LUID_VERIFY, IKEEXT_POLICY_FLAG_NO_MACHINE_LUID_VERIFY, fwp.ikeext_policy2, iketypes/IKEEXT_POLICY2, IKEEXT_POLICY_FLAG_POINT_TO_SITE
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IKEEXT_POLICY2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_POLICY2_
 - iketypes/IKEEXT_POLICY2_
 - IKEEXT_POLICY2
 - iketypes/IKEEXT_POLICY2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - iketypes.h
api_name:
 - IKEEXT_POLICY2
---

# IKEEXT_POLICY2 structure


## -description

The <b>IKEEXT_POLICY2</b> structure is used to store the IKE/AuthIP main mode negotiation policy.
[IKEEXT_POLICY0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_policy0)  is available.</div><div> </div>

## -struct-fields

### -field softExpirationTime

Type: <b>UINT32</b>

Lifetime of the IPsec soft SA, in seconds. The caller must set this to 0.

### -field numAuthenticationMethods

Type: <b>UINT32</b>

Number of authentication methods.

### -field authenticationMethods

Type: [IKEEXT_AUTHENTICATION_METHOD2](/windows/desktop/api/iketypes/ns-iketypes-ikeext_authentication_method2)*</b>

Array of acceptable authentication methods.

### -field initiatorImpersonationType

Type: <b><a href="/windows/win32/api/iketypes/ne-iketypes-ikeext_authentication_impersonation_type">IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE</a></b>

Type of impersonation. Applies only to AuthIP.

### -field numIkeProposals

Type: <b>UINT32</b>

Number of main mode proposals.

### -field ikeProposals

Type: [IKEEXT_PROPOSAL0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_proposal0)*</b>

Array of main mode proposals.

### -field flags

Type: <b>UINT32</b>

A combination of the following values.

<table>
<tr>
<th>IKE/AuthIP policy flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_POLICY_FLAG_DISABLE_DIAGNOSTICS"></a><a id="ikeext_policy_flag_disable_diagnostics"></a><dl>
<dt><b>IKEEXT_POLICY_FLAG_DISABLE_DIAGNOSTICS</b></dt>
</dl>
</td>
<td width="60%">
Disable special diagnostics mode for IKE/Authip. This will prevent IKE/AuthIp
from accepting unauthenticated notifications from peer, or sending MS_STATUS 
notifications to peer.

</td>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_POLICY_FLAG_NO_MACHINE_LUID_VERIFY"></a><a id="ikeext_policy_flag_no_machine_luid_verify"></a><dl>
<dt><b>IKEEXT_POLICY_FLAG_NO_MACHINE_LUID_VERIFY</b></dt>
</dl>
</td>
<td width="60%">
Disable SA verification of machine LUID.

</td>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_POLICY_FLAG_NO_IMPERSONATION_LUID_VERIFY"></a><a id="ikeext_policy_flag_no_impersonation_luid_verify"></a><dl>
<dt><b>IKEEXT_POLICY_FLAG_NO_IMPERSONATION_LUID_VERIFY</b></dt>
</dl>
</td>
<td width="60%">
Disable SA verification of machine impersonation LUID.

</td>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_POLICY_FLAG_ENABLE_OPTIONAL_DH"></a><a id="ikeext_policy_flag_enable_optional_dh"></a><dl>
<dt><b>IKEEXT_POLICY_FLAG_ENABLE_OPTIONAL_DH</b></dt>
</dl>
</td>
<td width="60%">
Allow the responder to accept any DH proposal, including no DH, regardless of what is configured in policy.  This flag is valid only if AuthIP is used.

</td>
</tr><tr>
<td width="40%"><a id="IKEEXT_POLICY_FLAG_POINT_TO_SITE"></a><a id="ikeext_policy_flag_point_to_site"></a><dl>
<dt><b>IKEEXT_POLICY_FLAG_POINT_TO_SITE</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the IKE policy is for Point-to-Site VPN connections, typically used by individual clients connecting to a virtual network.

</td>
</tr>
</table>

### -field maxDynamicFilters

Type: <b>UINT32</b>

Maximum number of dynamic IPsec filters per remote IP address and per 
   transport layer that is allowed to be added for any SA negotiated using 
   this policy. 

Set this to 0 to disable dynamic filter addition. Dynamic filters are added by IKE/AuthIP on responder, when the QM traffic proposed by initiator is a subset of responder's traffic configuration.

### -field retransmitDurationSecs

Type: <b>UINT32</b>

The number of seconds for which IKEv2 SA negotiation packets will be retransmitted before the SA times out. The caller must set this to at least 120 seconds.

## -see-also

<a href="/windows/win32/api/iketypes/ne-iketypes-ikeext_authentication_impersonation_type">IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE</a>



[IKEEXT_AUTHENTICATION_METHOD2](/windows/desktop/api/iketypes/ns-iketypes-ikeext_authentication_method2)



[IKEEXT_PROPOSAL0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_proposal0)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
