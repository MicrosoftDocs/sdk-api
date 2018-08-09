---
UID: NS:netioapi._MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES
title: "_MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES"
author: windows-sdk-content
description: Contains read-only information for the bandwidth estimates computed by the TCP/IP stack for a network connection.
old-location: mib\mib_ip_network_connection_bandwidth_estimates.htm
old-project: mib
ms.assetid: E3109F71-E103-4586-9274-B83C4DC22382
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*PMIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES, MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES, MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES structure [MIB], PMIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES, PMIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES structure pointer [MIB], _MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES, mib.mib_ip_network_connection_bandwidth_estimates, netioapi/MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES, netioapi/PMIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES, *PMIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Netioapi.h
api_name:
 - MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES structure


## -description


The 
<b>MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES</b> structure contains read-only information for the bandwidth estimates computed by the TCP/IP stack for a network connection. 


## -struct-fields




### -field InboundBandwidthInformation

Bandwidth estimates for the data being received by the host from the IP network.


### -field OutboundBandwidthInformation

Bandwidth estimates for the data being sent from the host to the IP network.


## -remarks



The 
<b>MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES</b> structure provides bandwidth estimates computed by the TCP/IP stack for a network connection. These bandwidth estimates are for the point of attachment of the host system to the underlying IP network. 

The <b>MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES</b> structure is used with the <a href="https://msdn.microsoft.com/FE60AF0D-15B0-4223-8AE1-3E65483A1C5F">GetIpNetworkConnectionBandwidthEstimates</a> function to return bandwidth estimates obtained for the point of attachment to the IP network. It is possible to have asymmetric deployments and network conditions where the estimates observed inbound and outbound differ from each other.

The  <b>MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES</b>  structure is defined in the <i>Netioapi.h</i> header file which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Netioapi.h</i> header file should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/FE60AF0D-15B0-4223-8AE1-3E65483A1C5F">GetIpNetworkConnectionBandwidthEstimates</a>



<a href="https://msdn.microsoft.com/291aabe7-a4e7-4cc7-9cf3-4a4bc021e15e">GetPerTcp6ConnectionEStats</a>



<a href="https://msdn.microsoft.com/71b9d795-6050-4a1a-9949-2c970801f52c">GetPerTcpConnectionEStats</a>



<a href="https://msdn.microsoft.com/F5D7238A-EAE0-4D60-A0A4-D839F738EF48">NL_BANDWIDTH_INFORMATION</a>



<a href="https://msdn.microsoft.com/330d06a2-9966-4e2b-b1bd-44c0f1b9416d">TCP_ESTATS_BANDWIDTH_ROD_v0</a>
 

 

