---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

