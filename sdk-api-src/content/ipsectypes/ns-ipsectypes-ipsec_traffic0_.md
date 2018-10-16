---
UID: NS:ipsectypes.IPSEC_TRAFFIC0_
title: IPSEC_TRAFFIC0_
author: windows-sdk-content
description: Specifies parameters to describe IPsec traffic.
old-location: fwp\ipsec_traffic0_struct.htm
tech.root: fwp
ms.assetid: 5be2da29-73d6-4381-8bde-3a3945ea7b5a
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IPSEC_TRAFFIC0, IPSEC_TRAFFIC0 structure [Filtering], IPSEC_TRAFFIC0_, fwp.ipsec_traffic0_struct, ipsectypes/IPSEC_TRAFFIC0
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
 - IPSEC_TRAFFIC0
product: Windows
targetos: Windows
req.typenames: IPSEC_TRAFFIC0
req.redist: 
---

# IPSEC_TRAFFIC0_ structure


## -description


The <b>IPSEC_TRAFFIC0</b> structure specifies parameters to describe IPsec traffic.
<div class="alert"><b>Note</b>  <b>IPSEC_TRAFFIC0</b> is the specific implementation of IPSEC_TRAFFIC used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://msdn.microsoft.com/2a3ad63f-9fa1-41c7-b628-5fe4e17ce7ac">IPSEC_TRAFFIC1</a> is available.</div><div> </div>

## -struct-fields




### -field ipVersion

Internet Protocol (IP) version. 

See <a href="https://msdn.microsoft.com/1712b83c-f32d-4981-9950-ab870a376182">FWP_IP_VERSION</a> for more information.


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

See <a href="https://msdn.microsoft.com/e87154ce-7f19-424c-a577-04e2eb81560e">IPSEC_TRAFFIC_TYPE</a> for more information.


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

For IPsec tunnel mode, the <b>localV*Address</b> and  <b>remoteV*Address</b> members specify the outer IP header tunnel endpoints. The <b>tunnelPolicyId</b> member specifies (as part of the filter conditions specified via <a href="https://msdn.microsoft.com/6de989e0-c5e1-4147-b5da-23448a4af2c9">FwpmIPsecTunnelAdd0</a>) the inner IP header addresses, transport protocol information, of the matching traffic. The <b>remotePort</b> member should not be specified for tunnel mode.




## -see-also




<a href="https://msdn.microsoft.com/1712b83c-f32d-4981-9950-ab870a376182">FWP_IP_VERSION</a>



<a href="https://msdn.microsoft.com/e87154ce-7f19-424c-a577-04e2eb81560e">IPSEC_TRAFFIC_TYPE</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

