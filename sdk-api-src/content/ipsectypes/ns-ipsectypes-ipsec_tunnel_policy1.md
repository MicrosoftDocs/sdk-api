---
UID: NS:ipsectypes.IPSEC_TUNNEL_POLICY1_
title: IPSEC_TUNNEL_POLICY1 (ipsectypes.h)
description: Stores the quick mode negotiation policy for tunnel mode IPsec. (IPSEC_TUNNEL_POLICY1)
helpviewer_keywords: ["IPSEC_POLICY_FLAG_CLEAR_DF_ON_TUNNEL","IPSEC_POLICY_FLAG_DONT_NEGOTIATE_BYTE_LIFETIME","IPSEC_POLICY_FLAG_DONT_NEGOTIATE_SECOND_LIFETIME","IPSEC_POLICY_FLAG_ENABLE_SERVER_ADDR_ASSIGNMENT","IPSEC_POLICY_FLAG_ENABLE_V6_IN_V4_TUNNELING","IPSEC_POLICY_FLAG_ND_BOUNDARY","IPSEC_POLICY_FLAG_ND_SECURE","IPSEC_POLICY_FLAG_TUNNEL_ALLOW_OUTBOUND_CLEAR_CONNECTION","IPSEC_POLICY_FLAG_TUNNEL_BYPASS_ALREADY_SECURE_CONNECTION","IPSEC_POLICY_FLAG_TUNNEL_BYPASS_ICMPV6","IPSEC_TUNNEL_POLICY1","IPSEC_TUNNEL_POLICY1 structure [Filtering]","fwp.ipsec_tunnel_policy1_struct","ipsectypes/IPSEC_TUNNEL_POLICY1"]
old-location: fwp\ipsec_tunnel_policy1_struct.htm
tech.root: fwp
ms.assetid: b51d330f-3f10-43e2-9018-eb6fd35ffe25
ms.date: 12/05/2018
ms.keywords: IPSEC_POLICY_FLAG_CLEAR_DF_ON_TUNNEL, IPSEC_POLICY_FLAG_DONT_NEGOTIATE_BYTE_LIFETIME, IPSEC_POLICY_FLAG_DONT_NEGOTIATE_SECOND_LIFETIME, IPSEC_POLICY_FLAG_ENABLE_SERVER_ADDR_ASSIGNMENT, IPSEC_POLICY_FLAG_ENABLE_V6_IN_V4_TUNNELING, IPSEC_POLICY_FLAG_ND_BOUNDARY, IPSEC_POLICY_FLAG_ND_SECURE, IPSEC_POLICY_FLAG_TUNNEL_ALLOW_OUTBOUND_CLEAR_CONNECTION, IPSEC_POLICY_FLAG_TUNNEL_BYPASS_ALREADY_SECURE_CONNECTION, IPSEC_POLICY_FLAG_TUNNEL_BYPASS_ICMPV6, IPSEC_TUNNEL_POLICY1, IPSEC_TUNNEL_POLICY1 structure [Filtering], fwp.ipsec_tunnel_policy1_struct, ipsectypes/IPSEC_TUNNEL_POLICY1
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
targetos: Windows
req.typenames: IPSEC_TUNNEL_POLICY1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_TUNNEL_POLICY1_
 - ipsectypes/IPSEC_TUNNEL_POLICY1_
 - IPSEC_TUNNEL_POLICY1
 - ipsectypes/IPSEC_TUNNEL_POLICY1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_TUNNEL_POLICY1
---

# IPSEC_TUNNEL_POLICY1 structure


## -description

The <b>IPSEC_TUNNEL_POLICY1</b> structure stores the quick mode negotiation policy for tunnel mode IPsec.
[IPSEC_TUNNEL_POLICY2](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2) is available.

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

See [IPSEC_PROPOSAL0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_proposal0) for more information.

### -field tunnelEndpoints

Tunnel endpoints of the IPsec security association (SA) generated from this policy.

See [IPSEC_TUNNEL_ENDPOINTS1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints1) for more information.

### -field saIdleTimeout

An [IPSEC_SA_IDLE_TIMEOUT0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_idle_timeout0) structure that specifies the SA idle timeout in IPsec policy.

### -field emPolicy

The AuthIP extended mode authentication policy.

See [IKEEXT_EM_POLICY1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_em_policy1) for more information.

## -see-also

[IKEEXT_EM_POLICY1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_em_policy1)



[IPSEC_PROPOSAL0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_proposal0)



[IPSEC_SA_IDLE_TIMEOUT0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_idle_timeout0)



<a href="/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints1">IPSEC_TUNNEL_ENDPOINTS1</a>



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
