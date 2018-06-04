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

# _NL_BANDWIDTH_INFORMATION structure


## -description


The <b>NL_BANDWIDTH_INFORMATION</b> structure contains read-only information on the available bandwidth estimates and associated variance as determined by the TCP/IP stack.


## -struct-fields




### -field Bandwidth

The estimated maximum available bandwidth, in bits per second.


### -field Instability

A measure of the variation based on recent bandwidth samples, in bits per second.


### -field BandwidthPeaked

A value that indicates if the bandwidth estimate in the <b>Bandwidth</b> member has peaked and reached its maximum value for the given network conditions. 

The TCP/IP stack uses a heuristic to set this variable. Until this variable is set, there is no guarantee that the true available maximum bandwidth is not higher than the estimated bandwidth in the <b>Bandwidth</b> member. However, it is safe to assume that maximum available bandwidth is not lower than the estimate reported in the <b>Bandwidth</b> member.


## -remarks



The  <b>NL_BANDWIDTH_INFORMATION</b> structure is defined in the <i>Nldef.h</i> header file which is automatically included by the <i>Iptypes.h</i> header file which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Nldef.h</i> and <i>Iptypes.h</i> header files should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/FE60AF0D-15B0-4223-8AE1-3E65483A1C5F">GetIpNetworkConnectionBandwidthEstimates</a>



<a href="https://msdn.microsoft.com/291aabe7-a4e7-4cc7-9cf3-4a4bc021e15e">GetPerTcp6ConnectionEStats</a>



<a href="https://msdn.microsoft.com/71b9d795-6050-4a1a-9949-2c970801f52c">GetPerTcpConnectionEStats</a>



<a href="https://msdn.microsoft.com/E3109F71-E103-4586-9274-B83C4DC22382">MIB_IP_NETWORK_CONNECTION_BANDWIDTH_ESTIMATES</a>



<a href="https://msdn.microsoft.com/330d06a2-9966-4e2b-b1bd-44c0f1b9416d">TCP_ESTATS_BANDWIDTH_ROD_v0</a>
 

 

