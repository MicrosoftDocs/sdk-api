---
UID: NS:ipsectypes.IPSEC_TRAFFIC1_
title: IPSEC_TRAFFIC1_
author: windows-driver-content
description: Specifies parameters to describe IPsec traffic.
old-location: fwp\ipsec_traffic1_struct.htm
old-project: FWP
ms.assetid: 2a3ad63f-9fa1-41c7-b628-5fe4e17ce7ac
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IPSEC_TRAFFIC1, IPSEC_TRAFFIC1 structure [Filtering], IPSEC_TRAFFIC1_, fwp.ipsec_traffic1_struct, ipsectypes/IPSEC_TRAFFIC1
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: IPSEC_TRAFFIC1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ipsectypes.h
api_name:
-	IPSEC_TRAFFIC1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPSEC_TRAFFIC1_ structure


## -description


The <b>IPSEC_TRAFFIC1</b> structure specifies parameters to describe IPsec traffic.
<div class="alert"><b>Note</b>  <b>IPSEC_TRAFFIC1</b> is the specific implementation of IPSEC_TRAFFIC used in Windows 7 and later. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista, <a href="https://msdn.microsoft.com/5be2da29-73d6-4381-8bde-3a3945ea7b5a">IPSEC_TRAFFIC0</a> is available.</div><div> </div>

## -struct-fields




### -field ipVersion

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff552435">FWP_IP_VERSION</a> value that specifies the IP version. In tunnel mode, this is the version of the outer header.


### -field trafficType

Type of IPsec traffic.

See <a href="https://msdn.microsoft.com/e87154ce-7f19-424c-a577-04e2eb81560e">IPSEC_TRAFFIC_TYPE</a> for more information.


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


#### - ipsecFilterId

The LUID of the FWPS transport
   layer filter corresponding to this traffic.

Available if <b>trafficType</b> is <b>IPSEC_TRAFFIC_TYPE_TRANSPORT</b>.


#### - localV4Address

The local IPv4 address of the IPsec traffic. In tunnel mode, this is the local tunnel endpoint.

Specified when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


#### - localV6Address

The local IPv6 address of the IPsec traffic. In tunnel mode, this is the local tunnel endpoint.

Specified when <b>ipVersion</b> is <b>FWP_IP_VERSION_V6</b>.


#### - remoteV4Address

The remote IPv4 address of the IPsec traffic. In tunnel mode, this is the remote tunnel endpoint.

Specified when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


#### - remoteV6Address

The remote IPv6 address of the IPsec traffic. In tunnel mode, this is the remote tunnel endpoint.

Specified when <b>ipVersion</b> is <b>FWP_IP_VERSION_V6</b>.


#### - tunnelPolicyId

The LUID of the associated Quick Mode (QM) tunnel policy. 

Available if <b>trafficType</b> is <b>IPSEC_TRAFFIC_TYPE_TUNNEL</b>.


## -remarks



The <b>IPSEC_TRAFFIC1</b> type describes the characteristics of the traffic that will match the SA. 

For IPsec transport mode, the <b>localV*Address</b> and  <b>remoteV*Address</b> members specify the IP addresses. The <b>ipsecFilterId</b> member specifies (as part of the transport layer filter conditions) the transport protocol information (such as IP protocol, ports, etc), of the matching traffic. However, if the <b>localPort</b>, <b>remotePort</b>, or <b>ipProtocol</b> member is nonzero, its value will override the corresponding value specified in the transport layer filter. 

For IPsec tunnel mode, the <b>localV*Address</b> and  <b>remoteV*Address</b> members specify the outer IP header tunnel endpoints. The <b>tunnelPolicyId</b> member specifies (as part of the filter conditions specified via <a href="https://msdn.microsoft.com/9ae40cf5-7ecf-4399-b196-ae58fe55afdb">FwpmIPsecTunnelAdd1</a>) the inner IP header addresses and transport protocol information of the matching traffic. The <b>localPort</b>, <b>remotePort</b>, and <b>ipProtocol</b> members should not be specified for tunnel mode.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552435">FWP_IP_VERSION</a>



<a href="https://msdn.microsoft.com/e87154ce-7f19-424c-a577-04e2eb81560e">IPSEC_TRAFFIC_TYPE</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

