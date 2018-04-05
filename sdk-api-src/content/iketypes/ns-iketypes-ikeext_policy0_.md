---
UID: NS:iketypes.IKEEXT_POLICY0_
title: IKEEXT_POLICY0_
author: windows-driver-content
description: Is used to store the IKE/AuthIP main mode negotiation policy.
old-location: fwp\ikeext_policy0.htm
old-project: FWP
ms.assetid: 4c33087a-2736-491c-a89f-e4b9ab136026
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IKEEXT_POLICY0, IKEEXT_POLICY0 structure [Filtering], IKEEXT_POLICY0_, IKEEXT_POLICY_FLAG_DISABLE_DIAGNOSTICS, IKEEXT_POLICY_FLAG_ENABLE_OPTIONAL_DH, IKEEXT_POLICY_FLAG_NO_IMPERSONATION_LUID_VERIFY, IKEEXT_POLICY_FLAG_NO_MACHINE_LUID_VERIFY, fwp.ikeext_policy0, iketypes/IKEEXT_POLICY0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IKEEXT_POLICY0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Iketypes.h
api_name:
-	IKEEXT_POLICY0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IKEEXT_POLICY0_ structure


## -description


The <b>IKEEXT_POLICY0</b> structure is used to store the IKE/AuthIP main mode negotiation policy.
<div class="alert"><b>Note</b>  <b>IKEEXT_POLICY0</b> is the specific implementation of IKEEXT_POLICY used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://msdn.microsoft.com/0834b147-9892-4afe-a5c8-cb782918a868">IKEEXT_POLICY1</a> is available.  For Windows 8, <a href="https://msdn.microsoft.com/d6efc1dd-3127-44d0-9f6a-ebf7cba477aa">IKEEXT_POLICY2</a> is available.</div><div> </div>

## -struct-fields




### -field softExpirationTime

Unused parameter, always set this to 0.


### -field numAuthenticationMethods

Number of authentication methods.


### -field authenticationMethods

Array of acceptable authentication methods.

See  <a href="https://msdn.microsoft.com/ce11d9ac-2636-432b-9bc7-3509f52478d9">IKEEXT_AUTHENTICATION_METHOD0</a> for more information.


### -field initiatorImpersonationType

Type of impersonation. Applies only to AuthIP. 

See <a href="https://msdn.microsoft.com/840c7429-5a1a-4e3f-823c-c46a412cbe71">IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE</a> for more information.


### -field numIkeProposals

Number of main mode proposals.


### -field ikeProposals

Array of main mode proposals. 

See <a href="https://msdn.microsoft.com/59568ef7-12bd-407a-a8ee-9bf261f49883">IKEEXT_PROPOSAL0</a> for more information.


### -field flags

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

Applicable only to  AuthIP.

</td>
</tr>
<tr>
<td width="40%"><a id="IKEEXT_POLICY_FLAG_ENABLE_OPTIONAL_DH"></a><a id="ikeext_policy_flag_enable_optional_dh"></a><dl>
<dt><b>IKEEXT_POLICY_FLAG_ENABLE_OPTIONAL_DH</b></dt>
</dl>
</td>
<td width="60%">
Allow the responder to accept any DH proposal, including no DH, regardless of what is configured in policy.

Applicable only to  AuthIP.

</td>
</tr>
</table>
 


### -field maxDynamicFilters

Maximum number of dynamic IPsec filters per remote IP address and per 
   transport layer that is allowed to be added for any SA negotiated using 
   this policy. 

Set this to 0 to disable dynamic filter addition. Dynamic filters are added by IKE/AuthIP on responder, when the QM traffic proposed by initiator is a subset of responder's traffic configuration. 


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

