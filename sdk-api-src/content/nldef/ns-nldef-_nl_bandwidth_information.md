---
UID: NS:nldef._NL_BANDWIDTH_INFORMATION
title: "_NL_BANDWIDTH_INFORMATION"
author: windows-sdk-content
description: Contains read-only information on the available bandwidth estimates and associated variance as determined by the TCP/IP stack.
old-location: iphlp\nl_bandwidth_information.htm
tech.root: IpHlp
ms.assetid: F5D7238A-EAE0-4D60-A0A4-D839F738EF48
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PNL_BANDWIDTH_INFORMATION, NL_BANDWIDTH_INFORMATION, NL_BANDWIDTH_INFORMATION structure [IP Helper], PNL_BANDWIDTH_INFORMATION, PNL_BANDWIDTH_INFORMATION structure pointer [IP Helper], _NL_BANDWIDTH_INFORMATION, iphlp.nl_bandwidth_information, nldef/NL_BANDWIDTH_INFORMATION, nldef/PNL_BANDWIDTH_INFORMATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: nldef.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Nldef.h
api_name:
 - NL_BANDWIDTH_INFORMATION
product: Windows
targetos: Windows
req.typenames: NL_BANDWIDTH_INFORMATION, *PNL_BANDWIDTH_INFORMATION
req.redist: 
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
 

 

