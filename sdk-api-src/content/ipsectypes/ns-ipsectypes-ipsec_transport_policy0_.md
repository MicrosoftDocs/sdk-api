---
UID: NS:ipsectypes.IPSEC_TRANSPORT_POLICY0_
title: IPSEC_TRANSPORT_POLICY0_
author: windows-sdk-content
description: Stores the quick mode negotiation policy for transport mode IPsec.
old-location: fwp\ipsec_transport_policy0_struct.htm
tech.root: fwp
ms.assetid: c17ebe74-41e3-467c-875a-db43978a5234
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IPSEC_POLICY_FLAG_DONT_NEGOTIATE_BYTE_LIFETIME, IPSEC_POLICY_FLAG_DONT_NEGOTIATE_SECOND_LIFETIME, IPSEC_POLICY_FLAG_NAT_ENCAP_ALLOW_GENERAL_NAT_TRAVERSAL, IPSEC_POLICY_FLAG_NAT_ENCAP_ALLOW_PEER_BEHIND_NAT, IPSEC_POLICY_FLAG_ND_BOUNDARY, IPSEC_POLICY_FLAG_ND_SECURE, IPSEC_TRANSPORT_POLICY0, IPSEC_TRANSPORT_POLICY0 structure [Filtering], IPSEC_TRANSPORT_POLICY0_, fwp.ipsec_transport_policy0_struct, ipsectypes/IPSEC_TRANSPORT_POLICY0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
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
 - Ipsectypes.h
api_name:
 - IPSEC_TRANSPORT_POLICY0
product: Windows
targetos: Windows
req.typenames: IPSEC_TRANSPORT_POLICY0
req.redist: 
---

# IPSEC_TRANSPORT_POLICY0_ structure


## -description


The <b>IPSEC_TRANSPORT_POLICY0</b> structure  stores the quick mode negotiation policy for transport mode IPsec.
<div class="alert"><b>Note</b>  <b>IPSEC_TRANSPORT_POLICY0</b> is the specific implementation of IPSEC_TRANSPORT_POLICY used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://msdn.microsoft.com/4ee39f30-f7fc-40a9-92b0-e059cb9b84a2">IPSEC_TRANSPORT_POLICY1</a> is available. For Windows 8, <a href="https://msdn.microsoft.com/fce0ce7e-770c-4cc6-94ea-21af0464f740">IPSEC_TRANSPORT_POLICY2</a> is available.</div><div> </div>

## -struct-fields




### -field numIpsecProposals

Number of quick mode proposals in the policy.


### -field ipsecProposals

Array of quick mode proposals.

See <a href="https://msdn.microsoft.com/bc551733-dbba-4d66-8054-fbf4bbfa28b5">IPSEC_PROPOSAL0</a> for more information.


### -field flags

A combination of the following values.

<table>
<tr>
<th>IPsec policy flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IPSEC_POLICY_FLAG_ND_SECURE"></a><a id="ipsec_policy_flag_nd_secure"></a><dl>
<dt><b>IPSEC_POLICY_FLAG_ND_SECURE</b></dt>
</dl>
</td>
<td width="60%">
Do negotiation discovery in secure ring.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_POLICY_FLAG_ND_BOUNDARY"></a><a id="ipsec_policy_flag_nd_boundary"></a><dl>
<dt><b>IPSEC_POLICY_FLAG_ND_BOUNDARY</b></dt>
</dl>
</td>
<td width="60%">
Do negotiation discovery in the untrusted perimeter zone.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_POLICY_FLAG_NAT_ENCAP_ALLOW_PEER_BEHIND_NAT"></a><a id="ipsec_policy_flag_nat_encap_allow_peer_behind_nat"></a><dl>
<dt><b>IPSEC_POLICY_FLAG_NAT_ENCAP_ALLOW_PEER_BEHIND_NAT</b></dt>
</dl>
</td>
<td width="60%">
If set, IPsec expects that either the local or remote machine is behind a network address translation (NAT) device, but not both.  This allows for less secure, but more flexible behavior.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_POLICY_FLAG_NAT_ENCAP_ALLOW_GENERAL_NAT_TRAVERSAL"></a><a id="ipsec_policy_flag_nat_encap_allow_general_nat_traversal"></a><dl>
<dt><b>IPSEC_POLICY_FLAG_NAT_ENCAP_ALLOW_GENERAL_NAT_TRAVERSAL</b></dt>
</dl>
</td>
<td width="60%">
If set, IPsec expects default ports when either the local, the remote, or both machines are behind a NAT device.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_POLICY_FLAG_DONT_NEGOTIATE_SECOND_LIFETIME"></a><a id="ipsec_policy_flag_dont_negotiate_second_lifetime"></a><dl>
<dt><b>IPSEC_POLICY_FLAG_DONT_NEGOTIATE_SECOND_LIFETIME</b></dt>
</dl>
</td>
<td width="60%">
If set, Internet Key Exchange (IKE) will not send the ISAKMP attribute for 'seconds'
lifetime during quick mode negotiation. 

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_POLICY_FLAG_DONT_NEGOTIATE_BYTE_LIFETIME"></a><a id="ipsec_policy_flag_dont_negotiate_byte_lifetime"></a><dl>
<dt><b>IPSEC_POLICY_FLAG_DONT_NEGOTIATE_BYTE_LIFETIME</b></dt>
</dl>
</td>
<td width="60%">
If set, IKE will not send the ISAKMP attribute for 'byte' lifetime during quick mode negotiation. 

</td>
</tr>
</table>
 


### -field ndAllowClearTimeoutSeconds

Timeout in seconds, after which the IPsec security association (SA) should stop accepting
   packets coming in the clear. Used for negotiation discovery.


### -field saIdleTimeout

An <a href="https://msdn.microsoft.com/99113c80-1e2a-4878-9b18-502cfb1e43cc">IPSEC_SA_IDLE_TIMEOUT0</a> structure that specifies the SA idle timeout in IPsec policy.


### -field emPolicy

The AuthIP extended mode authentication policy.

See <a href="https://msdn.microsoft.com/954a2bb8-eb54-4f41-8a0c-3f2af1190f57">IKEEXT_EM_POLICY0</a> for more information.


## -see-also




<a href="https://msdn.microsoft.com/954a2bb8-eb54-4f41-8a0c-3f2af1190f57">IKEEXT_EM_POLICY0</a>



<a href="https://msdn.microsoft.com/bc551733-dbba-4d66-8054-fbf4bbfa28b5">IPSEC_PROPOSAL0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

