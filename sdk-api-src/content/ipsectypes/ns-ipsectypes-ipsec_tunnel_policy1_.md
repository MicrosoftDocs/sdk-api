---
UID: NS:ipsectypes.IPSEC_TUNNEL_POLICY1_
title: IPSEC_TUNNEL_POLICY1_
author: windows-sdk-content
description: Stores the quick mode negotiation policy for tunnel mode IPsec.
old-location: fwp\ipsec_tunnel_policy1_struct.htm
tech.root: FWP
ms.assetid: b51d330f-3f10-43e2-9018-eb6fd35ffe25
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IPSEC_POLICY_FLAG_CLEAR_DF_ON_TUNNEL, IPSEC_POLICY_FLAG_DONT_NEGOTIATE_BYTE_LIFETIME, IPSEC_POLICY_FLAG_DONT_NEGOTIATE_SECOND_LIFETIME, IPSEC_POLICY_FLAG_ENABLE_SERVER_ADDR_ASSIGNMENT, IPSEC_POLICY_FLAG_ENABLE_V6_IN_V4_TUNNELING, IPSEC_POLICY_FLAG_ND_BOUNDARY, IPSEC_POLICY_FLAG_ND_SECURE, IPSEC_POLICY_FLAG_TUNNEL_ALLOW_OUTBOUND_CLEAR_CONNECTION, IPSEC_POLICY_FLAG_TUNNEL_BYPASS_ALREADY_SECURE_CONNECTION, IPSEC_POLICY_FLAG_TUNNEL_BYPASS_ICMPV6, IPSEC_TUNNEL_POLICY1, IPSEC_TUNNEL_POLICY1 structure [Filtering], IPSEC_TUNNEL_POLICY1_, fwp.ipsec_tunnel_policy1_struct, ipsectypes/IPSEC_TUNNEL_POLICY1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IPSEC_TUNNEL_POLICY1
product: Windows
targetos: Windows
req.typenames: IPSEC_TUNNEL_POLICY1
req.redist: 
---

# IPSEC_TUNNEL_POLICY1_ structure


## -description


The <b>IPSEC_TUNNEL_POLICY1</b> structure stores the quick mode negotiation policy for tunnel mode IPsec.
<div class="alert"><b>Note</b>  <b>IPSEC_TUNNEL_POLICY1</b> is the specific implementation of IPSEC_TUNNEL_POLICY used in Windows 7 and later. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista, <a href="https://msdn.microsoft.com/092b108c-47e1-4b2f-b7ed-184cf8abb392">IPSEC_TUNNEL_POLICY0</a> is available. For Windows 8, <a href="https://msdn.microsoft.com/a633505d-86ec-42ba-bb4c-3f61e8768eab">IPSEC_TUNNEL_POLICY2</a> is available.</div><div> </div>

## -struct-fields




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
<td width="40%"><a id="IPSEC_POLICY_FLAG_CLEAR_DF_ON_TUNNEL"></a><a id="ipsec_policy_flag_clear_df_on_tunnel"></a><dl>
<dt><b>IPSEC_POLICY_FLAG_CLEAR_DF_ON_TUNNEL</b></dt>
</dl>
</td>
<td width="60%">
 Clear the "DontFragment" bit on the outer IP header of an IPsec tunneled 
packet.

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
<tr>
<td width="40%"><a id="IPSEC_POLICY_FLAG_ENABLE_V6_IN_V4_TUNNELING"></a><a id="ipsec_policy_flag_enable_v6_in_v4_tunneling"></a><dl>
<dt><b>IPSEC_POLICY_FLAG_ENABLE_V6_IN_V4_TUNNELING</b></dt>
</dl>
</td>
<td width="60%">
Negotiate IPv6 inside IPv4 IPsec tunneling. Applicable only for tunnel mode policy, and supported only by IKEv2.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_POLICY_FLAG_ENABLE_SERVER_ADDR_ASSIGNMENT"></a><a id="ipsec_policy_flag_enable_server_addr_assignment"></a><dl>
<dt><b>IPSEC_POLICY_FLAG_ENABLE_SERVER_ADDR_ASSIGNMENT</b></dt>
</dl>
</td>
<td width="60%">
 Enable calls to RAS VPN server for address assignment. Applicable only for tunnel mode policy, and supported only by IKEv2.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_POLICY_FLAG_TUNNEL_ALLOW_OUTBOUND_CLEAR_CONNECTION"></a><a id="ipsec_policy_flag_tunnel_allow_outbound_clear_connection"></a><dl>
<dt><b>IPSEC_POLICY_FLAG_TUNNEL_ALLOW_OUTBOUND_CLEAR_CONNECTION</b></dt>
</dl>
</td>
<td width="60%">
 Allow outbound connections to bypass the tunnel policy. Applicable only for tunnel mode policy on a tunnel gateway. Do not set on a tunnel client.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_POLICY_FLAG_TUNNEL_BYPASS_ALREADY_SECURE_CONNECTION"></a><a id="ipsec_policy_flag_tunnel_bypass_already_secure_connection"></a><dl>
<dt><b>IPSEC_POLICY_FLAG_TUNNEL_BYPASS_ALREADY_SECURE_CONNECTION</b></dt>
</dl>
</td>
<td width="60%">
Allow ESP or UDP 500/4500 traffic to bypass the tunnel. Applicable only for tunnel mode policy.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_POLICY_FLAG_TUNNEL_BYPASS_ICMPV6"></a><a id="ipsec_policy_flag_tunnel_bypass_icmpv6"></a><dl>
<dt><b>IPSEC_POLICY_FLAG_TUNNEL_BYPASS_ICMPV6</b></dt>
</dl>
</td>
<td width="60%">
Allow ICMPv6 traffic to bypass the tunnel. Applicable only for tunnel mode policy.

</td>
</tr>
</table>
 


### -field numIpsecProposals

Number of quick mode proposals in the policy.


### -field ipsecProposals

Array of quick mode proposals.

See <a href="https://msdn.microsoft.com/bc551733-dbba-4d66-8054-fbf4bbfa28b5">IPSEC_PROPOSAL0</a> for more information.


### -field tunnelEndpoints

Tunnel endpoints of the IPsec security association (SA) generated from this policy.

See <a href="https://msdn.microsoft.com/125392f6-fa82-4d86-b8ac-8a481a2da42d">IPSEC_TUNNEL_ENDPOINTS1</a> for more information.


### -field saIdleTimeout

An <a href="https://msdn.microsoft.com/99113c80-1e2a-4878-9b18-502cfb1e43cc">IPSEC_SA_IDLE_TIMEOUT0</a> structure that specifies the SA idle timeout in IPsec policy.


### -field emPolicy

The AuthIP extended mode authentication policy.

See <a href="https://msdn.microsoft.com/dae56d71-31e0-4746-8bfb-4ade3705278f">IKEEXT_EM_POLICY1</a> for more information.


## -see-also




<a href="https://msdn.microsoft.com/dae56d71-31e0-4746-8bfb-4ade3705278f">IKEEXT_EM_POLICY1</a>



<a href="https://msdn.microsoft.com/bc551733-dbba-4d66-8054-fbf4bbfa28b5">IPSEC_PROPOSAL0</a>



<a href="https://msdn.microsoft.com/99113c80-1e2a-4878-9b18-502cfb1e43cc">IPSEC_SA_IDLE_TIMEOUT0</a>



<a href="https://msdn.microsoft.com/a37b13c7-61e4-49be-bd21-db3e7c9bcca5">IPSEC_TUNNEL_ENDPOINTS1</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

