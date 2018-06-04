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

# _TCP_ESTATS_BANDWIDTH_ROD_v0 structure


## -description


The <b>TCP_ESTATS_BANDWIDTH_ROD_v0</b> structure contains read-only dynamic information for extended TCP statistics on bandwidth estimation for a TCP connection.


## -struct-fields




### -field OutboundBandwidth

Type: <b>ULONG64</b>

The computed outbound bandwidth estimate, in bits per second, for the network path for the TCP connection.


### -field InboundBandwidth

Type: <b>ULONG64</b>

The computed inbound bandwidth estimate, in bits per second, for the network path for the TCP connection.


### -field OutboundInstability

Type: <b>ULONG64</b>

A measure, in bits per second, of the instability of the outbound bandwidth estimate for the network path for the TCP connection.


### -field InboundInstability

Type: <b>ULONG64</b>

A measure, in bits per second, of the instability of the inbound bandwidth estimate for the network path for the TCP connection.


### -field OutboundBandwidthPeaked

Type: <b>BOOLEAN</b>

A boolean value that indicates if the computed outbound bandwidth estimate for the network path for the TCP connection has reached its peak value.


### -field InboundBandwidthPeaked

Type: <b>BOOLEAN</b>

A boolean value that indicates if the computed inbound bandwidth estimate for the network path for the TCP connection has reached its peak value.


## -remarks



The <b>TCP_ESTATS_BANDWIDTH_ROD_v0</b> structure is used as part of the TCP extended statistics feature available on Windows Vista and later. 

The <b>TCP_ESTATS_BANDWIDTH_ROD_v0</b> is defined as version 0 of the structure for  read-only dynamic information for extended TCP statistics on bandwidth estimation for a TCP connection.  This information is available after the connection has been established.

The <b>TCP_ESTATS_BANDWIDTH_ROD_v0</b> structure is retrieved by calls to  the <a href="https://msdn.microsoft.com/291aabe7-a4e7-4cc7-9cf3-4a4bc021e15e">GetPerTcp6ConnectionEStats</a> or <a href="https://msdn.microsoft.com/71b9d795-6050-4a1a-9949-2c970801f52c">GetPerTcpConnectionEStats</a> functions when <b>TcpConnectionEstatsBandwidth</b> is passed in the <i>EstatsType</i> parameter. Extended TCP statistics need to be enabled to retrieve this structure.

The members of this structure are not defined in the IETF RFC on the TCP Extended Statistics MIB. For more information on this RFC, see <a href="http://go.microsoft.com/fwlink/p/?linkid=121686">http://www.ietf.org/rfc/rfc4898.txt</a>.





## -see-also




<a href="https://msdn.microsoft.com/FE60AF0D-15B0-4223-8AE1-3E65483A1C5F">GetIpNetworkConnectionBandwidthEstimates</a>



<a href="https://msdn.microsoft.com/291aabe7-a4e7-4cc7-9cf3-4a4bc021e15e">GetPerTcp6ConnectionEStats</a>



<a href="https://msdn.microsoft.com/71b9d795-6050-4a1a-9949-2c970801f52c">GetPerTcpConnectionEStats</a>



<a href="https://msdn.microsoft.com/F5D7238A-EAE0-4D60-A0A4-D839F738EF48">NL_BANDWIDTH_INFORMATION</a>



<a href="https://msdn.microsoft.com/96f55528-e74a-4360-a7a2-54ba19c3a284">TCP_ESTATS_TYPE</a>
 

 

