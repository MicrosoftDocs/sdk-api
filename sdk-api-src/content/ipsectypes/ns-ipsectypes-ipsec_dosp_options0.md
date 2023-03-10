---
UID: NS:ipsectypes.IPSEC_DOSP_OPTIONS0_
title: IPSEC_DOSP_OPTIONS0 (ipsectypes.h)
description: Used to store configuration parameters for IPsec DoS Protection.
helpviewer_keywords: ["IPSEC_DOSP_FLAG_DISABLE_AUTHIP","IPSEC_DOSP_FLAG_DISABLE_DEFAULT_BLOCK","IPSEC_DOSP_FLAG_ENABLE_IKEV1","IPSEC_DOSP_FLAG_ENABLE_IKEV2","IPSEC_DOSP_FLAG_FILTER_BLOCK","IPSEC_DOSP_FLAG_FILTER_EXEMPT","IPSEC_DOSP_OPTIONS0","IPSEC_DOSP_OPTIONS0 structure [Filtering]","fwp.ipsec_dosp_options0","ipsectypes/IPSEC_DOSP_OPTIONS0"]
old-location: fwp\ipsec_dosp_options0.htm
tech.root: fwp
ms.assetid: 7f180a05-ce8a-4f3b-8e97-d0b6f7f9f8ca
ms.date: 12/05/2018
ms.keywords: IPSEC_DOSP_FLAG_DISABLE_AUTHIP, IPSEC_DOSP_FLAG_DISABLE_DEFAULT_BLOCK, IPSEC_DOSP_FLAG_ENABLE_IKEV1, IPSEC_DOSP_FLAG_ENABLE_IKEV2, IPSEC_DOSP_FLAG_FILTER_BLOCK, IPSEC_DOSP_FLAG_FILTER_EXEMPT, IPSEC_DOSP_OPTIONS0, IPSEC_DOSP_OPTIONS0 structure [Filtering], fwp.ipsec_dosp_options0, ipsectypes/IPSEC_DOSP_OPTIONS0
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
req.typenames: IPSEC_DOSP_OPTIONS0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_DOSP_OPTIONS0_
 - ipsectypes/IPSEC_DOSP_OPTIONS0_
 - IPSEC_DOSP_OPTIONS0
 - ipsectypes/IPSEC_DOSP_OPTIONS0
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
 - IPSEC_DOSP_OPTIONS0
---

# IPSEC_DOSP_OPTIONS0 structure


## -description

The <b>IPSEC_DOSP_OPTIONS0</b> structure is used to store configuration parameters for IPsec DoS Protection.

## -struct-fields

### -field stateIdleTimeoutSeconds

The number of seconds before idle timeout. This value must be greater than 0.

### -field perIPRateLimitQueueIdleTimeoutSeconds

The idle timeout for the per IP rate limit queue object. This value must be greater than 0.

### -field ipV6IPsecUnauthDscp

The DSCP marking for unauthenticated inbound IPv6 IPsec traffic. This value must be less than or equal to 63. Specify IPSEC_DOSP_DSCP_DISABLE_VALUE to disable DSCP marking for this category.

### -field ipV6IPsecUnauthRateLimitBytesPerSec

The rate limit for unauthenticated inbound IPv6 IPsec traffic. Specify IPSEC_DOSP_RATE_LIMIT_DISABLE_VALUE to disable rate limiting for this category.

### -field ipV6IPsecUnauthPerIPRateLimitBytesPerSec

The rate limit for unauthenticated inbound IPv6 IPsec traffic per internal IP address. Specify IPSEC_DOSP_RATE_LIMIT_DISABLE_VALUE to disable rate limiting for this category.

### -field ipV6IPsecAuthDscp

The DSCP marking for authenticated inbound IPv6 IPsec traffic. The value must be less than or equal to 63. Specify IPSEC_DOSP_DSCP_DISABLE_VALUE to disable DSCP marking for this category.

### -field ipV6IPsecAuthRateLimitBytesPerSec

The rate limit for authenticated inbound IPv6 IPsec traffic. Specify IPSEC_DOSP_RATE_LIMIT_DISABLE_VALUE to disable rate limiting for this category..

### -field icmpV6Dscp

The DSCP marking for  inbound ICMPv6 traffic. The value must be less than or equal to 63. Specify IPSEC_DOSP_DSCP_DISABLE_VALUE to disable DSCP marking for this category.

### -field icmpV6RateLimitBytesPerSec

The rate limit for  inbound ICMPv6 traffic. Specify IPSEC_DOSP_RATE_LIMIT_DISABLE_VALUE to disable rate limiting for this category.

### -field ipV6FilterExemptDscp

The DSCP marking for  inbound IPv6 filter exempted traffic. The value must be less than or equal to 63. Specify IPSEC_DOSP_DSCP_DISABLE_VALUE to disable DSCP marking for this category.

### -field ipV6FilterExemptRateLimitBytesPerSec

The rate limit for  inbound IPV6 filter exempted traffic. Specify IPSEC_DOSP_RATE_LIMIT_DISABLE_VALUE to disable rate limiting for this category.

### -field defBlockExemptDscp

The DSCP marking for  inbound default-block exempted traffic. The value must be less than or equal to 63. Specify IPSEC_DOSP_DSCP_DISABLE_VALUE to disable DSCP marking for this category.

### -field defBlockExemptRateLimitBytesPerSec

The rate limit for  inbound default-block exempted traffic. Specify IPSEC_DOSP_RATE_LIMIT_DISABLE_VALUE to disable rate limiting for this category.

### -field maxStateEntries

The maximum number of state entries in the table. The value must be greater than 0.

### -field maxPerIPRateLimitQueues

The maximum number of rate limit queues for inbound unauthenticated IPv6 IPsec traffic per internal IP address. The value must be greater than 0.

### -field flags

A combination of the following values. 

<table>
<tr>
<th>IPsec DoS Protection options flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IPSEC_DOSP_FLAG_ENABLE_IKEV1"></a><a id="ipsec_dosp_flag_enable_ikev1"></a><dl>
<dt><b>IPSEC_DOSP_FLAG_ENABLE_IKEV1</b></dt>
</dl>
</td>
<td width="60%">
Allows the IKEv1 keying module. By default, it is blocked.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_DOSP_FLAG_ENABLE_IKEV2"></a><a id="ipsec_dosp_flag_enable_ikev2"></a><dl>
<dt><b>IPSEC_DOSP_FLAG_ENABLE_IKEV2</b></dt>
</dl>
</td>
<td width="60%">
Allows the IKEv2 keying module. By default, it is blocked.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_DOSP_FLAG_DISABLE_AUTHIP"></a><a id="ipsec_dosp_flag_disable_authip"></a><dl>
<dt><b>IPSEC_DOSP_FLAG_DISABLE_AUTHIP</b></dt>
</dl>
</td>
<td width="60%">
Blocks the AuthIP keying module. By default, it is allowed.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_DOSP_FLAG_DISABLE_DEFAULT_BLOCK"></a><a id="ipsec_dosp_flag_disable_default_block"></a><dl>
<dt><b>IPSEC_DOSP_FLAG_DISABLE_DEFAULT_BLOCK</b></dt>
</dl>
</td>
<td width="60%">
Allows all matching IPv4 traffic and non-IPsec IPv6 traffic. By default, all IPv4 traffic and non-IPsecIPv6 traffic, except IPv6 ICMP, will be blocked.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_DOSP_FLAG_FILTER_BLOCK"></a><a id="ipsec_dosp_flag_filter_block"></a><dl>
<dt><b>IPSEC_DOSP_FLAG_FILTER_BLOCK</b></dt>
</dl>
</td>
<td width="60%">
Blocks all matching IPv6 traffic.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_DOSP_FLAG_FILTER_EXEMPT"></a><a id="ipsec_dosp_flag_filter_exempt"></a><dl>
<dt><b>IPSEC_DOSP_FLAG_FILTER_EXEMPT</b></dt>
</dl>
</td>
<td width="60%">
Allows all matching IPv6 traffic.

</td>
</tr>
</table>

### -field numPublicIFLuids

The number  of public Internet facing interface identifiers for which DOS protection should be enabled.

### -field publicIFLuids

Pointer to an array of public Internet facing interface identifiers for which DOS protection should be enabled.

### -field numInternalIFLuids

The number of internal network facing interface identifiers for which DOS protection should be enabled.

### -field internalIFLuids

Pointer to an array of internal network facing interface identifiers for which DOS protection should be enabled.

### -field publicV6AddrMask

Optional public IPv6 address or subnet for this policy, as specified in [FWP_V6_ADDR_AND_MASK](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_v6_addr_and_mask).

### -field internalV6AddrMask

Optional internal IPv6 address or subnet for this policy, as specified in [FWP_V6_ADDR_AND_MASK](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_v6_addr_and_mask).

## -remarks

<b>IPSEC_DOSP_OPTIONS0</b> is a specific implementation of IPSEC_DOSP_OPTIONS. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWP_V6_ADDR_AND_MASK](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_v6_addr_and_mask)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>