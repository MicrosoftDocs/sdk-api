---
UID: NS:ipsectypes.IPSEC_TUNNEL_POLICY0_
title: IPSEC_TUNNEL_POLICY0 (ipsectypes.h)
author: windows-sdk-content
description: Stores the quick mode negotiation policy for tunnel mode IPsec.
old-location: fwp\ipsec_tunnel_policy0_struct.htm
tech.root: fwp
ms.assetid: 092b108c-47e1-4b2f-b7ed-184cf8abb392
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPSEC_POLICY_FLAG_CLEAR_DF_ON_TUNNEL, IPSEC_POLICY_FLAG_DONT_NEGOTIATE_BYTE_LIFETIME, IPSEC_POLICY_FLAG_DONT_NEGOTIATE_SECOND_LIFETIME, IPSEC_POLICY_FLAG_ND_BOUNDARY, IPSEC_POLICY_FLAG_ND_SECURE, IPSEC_TUNNEL_POLICY0, IPSEC_TUNNEL_POLICY0 structure [Filtering], fwp.ipsec_tunnel_policy0_struct, ipsectypes/IPSEC_TUNNEL_POLICY0
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
 - IPSEC_TUNNEL_POLICY0
product: Windows
targetos: Windows
req.typenames: IPSEC_TUNNEL_POLICY0
req.redist: 
ms.custom: 19H1
---

# IPSEC_TUNNEL_POLICY0 structure


## -description


The <b>IPSEC_TUNNEL_POLICY0</b> structure  stores the quick mode negotiation policy for tunnel mode IPsec.
<div class="alert"><b>Note</b>  <b>IPSEC_TUNNEL_POLICY0</b> is the specific implementation of IPSEC_TUNNEL_POLICY used in Windows Vista. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy1_">IPSEC_TUNNEL_POLICY1</a> is available. For Windows 8, <a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2_">IPSEC_TUNNEL_POLICY2</a> is available.</div><div> </div>

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
</table>
 


### -field numIpsecProposals

Number of quick mode proposals in the policy.


### -field ipsecProposals

Array of quick mode proposals.

See <a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_proposal0_">IPSEC_PROPOSAL0</a> for more information.


### -field tunnelEndpoints

Tunnel endpoints of the IPsec security association (SA) generated from this policy.

See <a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints0_">IPSEC_TUNNEL_ENDPOINTS0</a> for more information.


### -field saIdleTimeout

An <a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_idle_timeout0_">IPSEC_SA_IDLE_TIMEOUT0</a> structure that specifies the SA idle timeout in IPsec policy.


### -field emPolicy

The AuthIP extended mode authentication policy.

See <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_em_policy0_">IKEEXT_EM_POLICY0</a> for more information.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_em_policy0_">IKEEXT_EM_POLICY0</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_proposal0_">IPSEC_PROPOSAL0</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_idle_timeout0_">IPSEC_SA_IDLE_TIMEOUT0</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints0_">IPSEC_TUNNEL_ENDPOINTS0</a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

