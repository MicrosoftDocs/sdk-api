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

# _TCP_INITIAL_RTO_PARAMETERS structure


## -description



			The 
<a href="https://msdn.microsoft.com/862dd8f8-5929-4426-b531-a87e36506634">TCP_INITIAL_RTO_PARAMETERS</a> structure  specifies data used by the <a href="https://msdn.microsoft.com/F5ABAE57-E0F0-4AEB-825C-B53AEE8210E7">SIO_TCP_INITIAL_RTO</a> IOCTL to configure initial re-transmission timeout (RTO) parameters to be used on the socket.


## -struct-fields




### -field Rtt

Supplies the initial RTT in milliseconds.


### -field MaxSynRetransmissions

Supplies the number of retransmissions attempted before the connection
    setup fails.



## -remarks



The <a href="https://msdn.microsoft.com/862dd8f8-5929-4426-b531-a87e36506634">TCP_INITIAL_RTO_PARAMETERS</a> structure  allows an application to configure the initial round trip time (RTT) used to compute the retransmission timeout. The application can also configure the number of re-transmissions that will be attempted before the connection attempt fails. 

An application should supply the RTT of choice in milliseconds and the maximum number of retransmissions in this structure. The Windows TCP/IP stack will honor these parameters for the subsequent connection attempt. The retransmission behavior for TCP is documented in IETF RFC 793 and 2988.

An application may use the unspecified defines,  <b>TCP_INITIAL_RTO_UNSPECIFIED_RTT</b> and <b>TCP_INITIAL_RTO_UNSPECIFIED_MAX_SYN_RETRANSMISSIONS</b>  when supplying values for one of these fields. This allows the system to pick up administrator configured settings for the parameter left unspecified.

An application can choose system defaults for any of these fields and supply those values using the default defines, <b>TCP_INITIAL_RTO_DEFAULT_RTT</b> and <b>TCP_INITIAL_RTO_DEFAULT_MAX_SYN_RETRANSMISSIONS</b>.




## -see-also




<a href="https://msdn.microsoft.com/F5ABAE57-E0F0-4AEB-825C-B53AEE8210E7">SIO_TCP_INITIAL_RTO</a>
 

 

