---
UID: NS:ipsectypes.IPSEC_SA_BUNDLE0_
title: IPSEC_SA_BUNDLE0 (ipsectypes.h)
description: Is used to store information about an IPsec security association (SA) bundle. (IPSEC_SA_BUNDLE0)
helpviewer_keywords: ["IPSEC_SA_BUNDLE0","IPSEC_SA_BUNDLE0 structure [Filtering]","IPSEC_SA_BUNDLE_FLAG_ALLOW_NULL_TARGET_NAME_MATCH","IPSEC_SA_BUNDLE_FLAG_ASSUME_UDP_CONTEXT_OUTBOUND","IPSEC_SA_BUNDLE_FLAG_CLEAR_DF_ON_TUNNEL","IPSEC_SA_BUNDLE_FLAG_GUARANTEE_ENCRYPTION","IPSEC_SA_BUNDLE_FLAG_ND_BOUNDARY","IPSEC_SA_BUNDLE_FLAG_ND_PEER_BOUNDARY","IPSEC_SA_BUNDLE_FLAG_ND_PEER_NAT_BOUNDARY","IPSEC_SA_BUNDLE_FLAG_ND_SECURE","IPSEC_SA_BUNDLE_FLAG_NLB","IPSEC_SA_BUNDLE_FLAG_NO_EXPLICIT_CRED_MATCH","IPSEC_SA_BUNDLE_FLAG_NO_IMPERSONATION_LUID_VERIFY","IPSEC_SA_BUNDLE_FLAG_NO_MACHINE_LUID_VERIFY","fwp.ipsec_sa_bundle0_struct","ipsectypes/IPSEC_SA_BUNDLE0"]
old-location: fwp\ipsec_sa_bundle0_struct.htm
tech.root: fwp
ms.assetid: 65376dd9-e06c-41ff-8689-74be12c47239
ms.date: 12/05/2018
ms.keywords: IPSEC_SA_BUNDLE0, IPSEC_SA_BUNDLE0 structure [Filtering], IPSEC_SA_BUNDLE_FLAG_ALLOW_NULL_TARGET_NAME_MATCH, IPSEC_SA_BUNDLE_FLAG_ASSUME_UDP_CONTEXT_OUTBOUND, IPSEC_SA_BUNDLE_FLAG_CLEAR_DF_ON_TUNNEL, IPSEC_SA_BUNDLE_FLAG_GUARANTEE_ENCRYPTION, IPSEC_SA_BUNDLE_FLAG_ND_BOUNDARY, IPSEC_SA_BUNDLE_FLAG_ND_PEER_BOUNDARY, IPSEC_SA_BUNDLE_FLAG_ND_PEER_NAT_BOUNDARY, IPSEC_SA_BUNDLE_FLAG_ND_SECURE, IPSEC_SA_BUNDLE_FLAG_NLB, IPSEC_SA_BUNDLE_FLAG_NO_EXPLICIT_CRED_MATCH, IPSEC_SA_BUNDLE_FLAG_NO_IMPERSONATION_LUID_VERIFY, IPSEC_SA_BUNDLE_FLAG_NO_MACHINE_LUID_VERIFY, fwp.ipsec_sa_bundle0_struct, ipsectypes/IPSEC_SA_BUNDLE0
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
targetos: Windows
req.typenames: IPSEC_SA_BUNDLE0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_SA_BUNDLE0_
 - ipsectypes/IPSEC_SA_BUNDLE0_
 - IPSEC_SA_BUNDLE0
 - ipsectypes/IPSEC_SA_BUNDLE0
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
 - IPSEC_SA_BUNDLE0
---

# IPSEC_SA_BUNDLE0 structure


## -description

The <b>IPSEC_SA_BUNDLE0</b> structure is used to store information about an IPsec security association (SA) bundle.
[IPSEC_SA_BUNDLE1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_bundle1) is available.</div><div> </div>

## -struct-fields

### -field flags

A combination of the following values.

<table>
<tr>
<th>IPsec SA bundle flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IPSEC_SA_BUNDLE_FLAG_ND_SECURE"></a><a id="ipsec_sa_bundle_flag_nd_secure"></a><dl>
<dt><b>IPSEC_SA_BUNDLE_FLAG_ND_SECURE</b></dt>
</dl>
</td>
<td width="60%">
Negotiation discovery is enabled in secure ring.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_SA_BUNDLE_FLAG_ND_BOUNDARY"></a><a id="ipsec_sa_bundle_flag_nd_boundary"></a><dl>
<dt><b>IPSEC_SA_BUNDLE_FLAG_ND_BOUNDARY</b></dt>
</dl>
</td>
<td width="60%">
Negotiation discovery in enabled in the untrusted perimeter zone.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_SA_BUNDLE_FLAG_ND_PEER_NAT_BOUNDARY"></a><a id="ipsec_sa_bundle_flag_nd_peer_nat_boundary"></a><dl>
<dt><b>IPSEC_SA_BUNDLE_FLAG_ND_PEER_NAT_BOUNDARY</b></dt>
</dl>
</td>
<td width="60%">
Peer is in untrusted perimeter zone ring and a NAT is in the way. Used with negotiation discovery.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_SA_BUNDLE_FLAG_GUARANTEE_ENCRYPTION"></a><a id="ipsec_sa_bundle_flag_guarantee_encryption"></a><dl>
<dt><b>IPSEC_SA_BUNDLE_FLAG_GUARANTEE_ENCRYPTION</b></dt>
</dl>
</td>
<td width="60%">
Indicates that this is an SA for connections that require guaranteed encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="_IPSEC_SA_BUNDLE_FLAG_NLB"></a><a id="_ipsec_sa_bundle_flag_nlb"></a><dl>
<dt><b>	IPSEC_SA_BUNDLE_FLAG_NLB</b></dt>
</dl>
</td>
<td width="60%">
Indicates that this is an SA to an NLB server.

</td>
</tr>
<tr>
<td width="40%"><a id="_IPSEC_SA_BUNDLE_FLAG_NO_MACHINE_LUID_VERIFY"></a><a id="_ipsec_sa_bundle_flag_no_machine_luid_verify"></a><dl>
<dt><b>	IPSEC_SA_BUNDLE_FLAG_NO_MACHINE_LUID_VERIFY</b></dt>
</dl>
</td>
<td width="60%">
Indicates that this SA should bypass machine LUID verification.

</td>
</tr>
<tr>
<td width="40%"><a id="_IPSEC_SA_BUNDLE_FLAG_NO_IMPERSONATION_LUID_VERIFY"></a><a id="_ipsec_sa_bundle_flag_no_impersonation_luid_verify"></a><dl>
<dt><b>	IPSEC_SA_BUNDLE_FLAG_NO_IMPERSONATION_LUID_VERIFY</b></dt>
</dl>
</td>
<td width="60%">
Indicates that this SA should bypass impersonation LUID verification.

</td>
</tr>
<tr>
<td width="40%"><a id="_IPSEC_SA_BUNDLE_FLAG_NO_EXPLICIT_CRED_MATCH"></a><a id="_ipsec_sa_bundle_flag_no_explicit_cred_match"></a><dl>
<dt><b>	IPSEC_SA_BUNDLE_FLAG_NO_EXPLICIT_CRED_MATCH</b></dt>
</dl>
</td>
<td width="60%">
Indicates that this SA should bypass explicit credential handle matching.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_SA_BUNDLE_FLAG_ALLOW_NULL_TARGET_NAME_MATCH"></a><a id="ipsec_sa_bundle_flag_allow_null_target_name_match"></a><dl>
<dt><b>IPSEC_SA_BUNDLE_FLAG_ALLOW_NULL_TARGET_NAME_MATCH</b></dt>
</dl>
</td>
<td width="60%">
Allows an SA formed with a peer name to carry traffic that does not have an associated peer target.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_SA_BUNDLE_FLAG_CLEAR_DF_ON_TUNNEL"></a><a id="ipsec_sa_bundle_flag_clear_df_on_tunnel"></a><dl>
<dt><b>IPSEC_SA_BUNDLE_FLAG_CLEAR_DF_ON_TUNNEL</b></dt>
</dl>
</td>
<td width="60%">
Clears the <b>DontFragment</b> bit on the outer IP header of an IPsec-tunneled packet. This flag is applicable only to tunnel mode SAs.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_SA_BUNDLE_FLAG_ASSUME_UDP_CONTEXT_OUTBOUND"></a><a id="ipsec_sa_bundle_flag_assume_udp_context_outbound"></a><dl>
<dt><b>IPSEC_SA_BUNDLE_FLAG_ASSUME_UDP_CONTEXT_OUTBOUND</b></dt>
</dl>
</td>
<td width="60%">
Default encapsulation ports (4500 and 4000) can be used when matching this SA with packets on outbound connections that do not have an associated IPsec-NAT-shim context.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_SA_BUNDLE_FLAG_ND_PEER_BOUNDARY"></a><a id="ipsec_sa_bundle_flag_nd_peer_boundary"></a><dl>
<dt><b>IPSEC_SA_BUNDLE_FLAG_ND_PEER_BOUNDARY</b></dt>
</dl>
</td>
<td width="60%">
Peer has negotiation discovery enabled, and is on a perimeter network.

</td>
</tr>
</table>

### -field lifetime

Lifetime of all the SAs in the bundle as specified by [IPSEC_SA_LIFETIME0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_lifetime0).

### -field idleTimeoutSeconds

Timeout in seconds after which the SAs in the bundle will idle out (due to traffic inactivity) and expire.

### -field ndAllowClearTimeoutSeconds

Timeout in seconds, after which the IPsec SA should stop accepting
   packets coming in the clear. 

Used for negotiation discovery.

### -field ipsecId

Pointer to an [IPSEC_ID0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_id0) structure that contains optional IPsec identity info.

### -field napContext

Network Access Protection (NAP) peer credentials information.

### -field qmSaId

SA identifier used by IPsec when choosing the SA to expire.  For an IPsec SA pair, the <b>qmSaId</b> must be the same between the initiating and responding machines and across inbound and outbound SA bundles.  For different IPsec pairs, the <b>qmSaId</b> must be different.

### -field numSAs

Number of SAs in the bundle. The only possible values are 1 and 2. Use 2 only when specifying AH + ESP SAs.

### -field saList

Array of IPsec SAs in the bundle. For AH + ESP SAs, use index [0] for ESP SA and index [1] for AH SA.



See [IPSEC_SA0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa0) for more information.

### -field keyModuleState

Optional keying module specific information as specified by [IPSEC_KEYMODULE_STATE0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_keymodule_state0).

### -field ipVersion

IP version as specified by [FWP_IP_VERSION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version).

### -field peerV4PrivateAddress

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>. If peer is behind a network address translation (NAT) device, this member stores the peer's 
   private address.

### -field mmSaId

Use this ID to correlate this IPsec SA with the IKE SA that generated it.

### -field pfsGroup

 Specifies whether Quick Mode perfect forward secrecy (PFS) was enabled for
   this SA, and if so, contains the Diffie-Hellman group that was used for
   PFS.

See [IPSEC_PFS_GROUP](/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_pfs_group) for more information.

## -see-also

[FWP_IP_VERSION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version)



[IPSEC_KEYMODULE_STATE0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_keymodule_state0)



[IPSEC_PFS_GROUP](/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_pfs_group)



[IPSEC_SA0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa0)



[IPSEC_SA_LIFETIME0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_lifetime0)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
