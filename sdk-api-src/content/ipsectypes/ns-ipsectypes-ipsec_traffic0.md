---
UID: NS:ipsectypes.IPSEC_TRAFFIC0_
title: IPSEC_TRAFFIC0 (ipsectypes.h)
description: Specifies parameters to describe IPsec traffic. (IPSEC_TRAFFIC0)
helpviewer_keywords: ["IPSEC_TRAFFIC0","IPSEC_TRAFFIC0 structure [Filtering]","fwp.ipsec_traffic0_struct","ipsectypes/IPSEC_TRAFFIC0"]
old-location: fwp\ipsec_traffic0_struct.htm
tech.root: fwp
ms.assetid: 5be2da29-73d6-4381-8bde-3a3945ea7b5a
ms.date: 12/05/2018
ms.keywords: IPSEC_TRAFFIC0, IPSEC_TRAFFIC0 structure [Filtering], fwp.ipsec_traffic0_struct, ipsectypes/IPSEC_TRAFFIC0
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
req.typenames: IPSEC_TRAFFIC0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_TRAFFIC0_
 - ipsectypes/IPSEC_TRAFFIC0_
 - IPSEC_TRAFFIC0
 - ipsectypes/IPSEC_TRAFFIC0
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
 - IPSEC_TRAFFIC0
---

# IPSEC_TRAFFIC0 structure


## -description

The <b>IPSEC_TRAFFIC0</b> structure specifies parameters to describe IPsec traffic.
[IPSEC_TRAFFIC1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_traffic1) is available.</div><div> </div>

## -struct-fields

### -field ipVersion

Internet Protocol (IP) version. 

See [FWP_IP_VERSION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version) for more information.

### -field localV4Address

The local IPv4 address of the IPsec traffic. 

Specified when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.

### -field localV6Address

The local IPv6 address of the IPsec traffic.

Specified when <b>ipVersion</b> is <b>FWP_IP_VERSION_V6</b>.

### -field remoteV4Address

The remote IPv4 address of the IPsec traffic. 

Specified when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.

### -field remoteV6Address

The remote IPv6 address of the IPsec traffic. 

Specified when <b>ipVersion</b> is <b>FWP_IP_VERSION_V6</b>.

### -field trafficType

Type of IPsec traffic.

See [IPSEC_TRAFFIC_TYPE](/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_traffic_type) for more information.

### -field ipsecFilterId

The LUID of the FWPS transport
   layer filter corresponding to this traffic. 

Available if <b>trafficType</b> is <b>IPSEC_TRAFFIC_TYPE_TRANSPORT</b>.

### -field tunnelPolicyId

The LUID of the associated Quick Mode (QM) tunnel policy. 

Available if <b>trafficType</b> is <b>IPSEC_TRAFFIC_TYPE_TUNNEL</b>.

### -field remotePort

The remote TCP/UDP port for this traffic. This is used when the remote port condition in the transport
   layer filter is more generic than the actual remote port.

## -remarks

The <b>IPSEC_TRAFFIC0</b> type describes the characteristics of the traffic that will match the SA. 

For IPsec transport mode, the <b>localV*Address</b> and  <b>remoteV*Address</b> members specify the IP addresses. The <b>ipsecFilterId</b> member specifies (as part of the transport layer filter conditions) the transport protocol information (such as IP protocol, ports, etc), of the matching traffic. However, if the <b>remotePort</b> member is nonzero, its value will override the remote port specified in the transport layer filter. 

For IPsec tunnel mode, the <b>localV*Address</b> and  <b>remoteV*Address</b> members specify the outer IP header tunnel endpoints. The <b>tunnelPolicyId</b> member specifies (as part of the filter conditions specified via <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd0">FwpmIPsecTunnelAdd0</a>) the inner IP header addresses, transport protocol information, of the matching traffic. The <b>remotePort</b> member should not be specified for tunnel mode.

## -see-also

[FWP_IP_VERSION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version)



[IPSEC_TRAFFIC_TYPE](/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_traffic_type)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
