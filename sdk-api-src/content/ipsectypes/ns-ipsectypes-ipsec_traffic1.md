---
UID: NS:ipsectypes.IPSEC_TRAFFIC1_
title: IPSEC_TRAFFIC1 (ipsectypes.h)
description: Specifies parameters to describe IPsec traffic. (IPSEC_TRAFFIC1)
helpviewer_keywords: ["IPSEC_TRAFFIC1","IPSEC_TRAFFIC1 structure [Filtering]","fwp.ipsec_traffic1_struct","ipsectypes/IPSEC_TRAFFIC1"]
old-location: fwp\ipsec_traffic1_struct.htm
tech.root: fwp
ms.assetid: 2a3ad63f-9fa1-41c7-b628-5fe4e17ce7ac
ms.date: 12/05/2018
ms.keywords: IPSEC_TRAFFIC1, IPSEC_TRAFFIC1 structure [Filtering], fwp.ipsec_traffic1_struct, ipsectypes/IPSEC_TRAFFIC1
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
req.typenames: IPSEC_TRAFFIC1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_TRAFFIC1_
 - ipsectypes/IPSEC_TRAFFIC1_
 - IPSEC_TRAFFIC1
 - ipsectypes/IPSEC_TRAFFIC1
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
 - IPSEC_TRAFFIC1
---

# IPSEC_TRAFFIC1 structure


## -description

The <b>IPSEC_TRAFFIC1</b> structure specifies parameters to describe IPsec traffic.
[IPSEC_TRAFFIC0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_traffic0) is available.</div><div> </div>

## -struct-fields

### -field ipVersion

An [FWP_IP_VERSION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version) value that specifies the IP version. In tunnel mode, this is the version of the outer header.

### -field localV4Address

The local IPv4 address of the IPsec traffic. In tunnel mode, this is the local tunnel endpoint.

Specified when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.

### -field localV6Address

The local IPv6 address of the IPsec traffic. In tunnel mode, this is the local tunnel endpoint.

Specified when <b>ipVersion</b> is <b>FWP_IP_VERSION_V6</b>.

### -field remoteV4Address

The remote IPv4 address of the IPsec traffic. In tunnel mode, this is the remote tunnel endpoint.

Specified when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.

### -field remoteV6Address

The remote IPv6 address of the IPsec traffic. In tunnel mode, this is the remote tunnel endpoint.

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

### -field localPort

The local TCP/UDP port for this traffic. This is used when the local port condition in the transport
   layer filter is more generic than the actual local port.

### -field ipProtocol

The IP protocol for this traffic. This is used when the IP protocol condition in the transport
   layer filter is more generic than the actual IP protocol.

### -field localIfLuid

The LUID of the local interface corresponding to the local address specified above.

### -field realIfProfileId

The profile ID corresponding to the actual interface that the traffic is using.

## -remarks

The <b>IPSEC_TRAFFIC1</b> type describes the characteristics of the traffic that will match the SA. 

For IPsec transport mode, the <b>localV*Address</b> and  <b>remoteV*Address</b> members specify the IP addresses. The <b>ipsecFilterId</b> member specifies (as part of the transport layer filter conditions) the transport protocol information (such as IP protocol, ports, etc), of the matching traffic. However, if the <b>localPort</b>, <b>remotePort</b>, or <b>ipProtocol</b> member is nonzero, its value will override the corresponding value specified in the transport layer filter. 

For IPsec tunnel mode, the <b>localV*Address</b> and  <b>remoteV*Address</b> members specify the outer IP header tunnel endpoints. The <b>tunnelPolicyId</b> member specifies (as part of the filter conditions specified via <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd1">FwpmIPsecTunnelAdd1</a>) the inner IP header addresses and transport protocol information of the matching traffic. The <b>localPort</b>, <b>remotePort</b>, and <b>ipProtocol</b> members should not be specified for tunnel mode.

## -see-also

[FWP_IP_VERSION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version)



[IPSEC_TRAFFIC_TYPE](/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_traffic_type)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
