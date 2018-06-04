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

# _MIB_IPPATH_ROW structure


## -description


The 
<b>MIB_IPPATH_ROW</b> structure stores information about an IP path entry.


## -struct-fields




### -field Source

Type: <b><a href="https://msdn.microsoft.com/7278dcb4-65c6-4aea-a474-cb7fae4d7672">SOCKADDR_INET</a></b>

The source IP address for this IP path entry. 


### -field Destination

Type: <b><a href="https://msdn.microsoft.com/7278dcb4-65c6-4aea-a474-cb7fae4d7672">SOCKADDR_INET</a></b>

The destination IP address for this IP path entry. 


### -field InterfaceLuid

Type: <b>NET_LUID</b>

The locally unique identifier (LUID) for the network interface associated with this IP path entry.


### -field InterfaceIndex

Type: <b>NET_IFINDEX</b>

The local index value for the network interface associated with this IP path entry. This index value may change when a network adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent. 


### -field CurrentNextHop

Type: <b><a href="https://msdn.microsoft.com/7278dcb4-65c6-4aea-a474-cb7fae4d7672">SOCKADDR_INET</a></b>

The current IP address of the next system or gateway en route. This member can change over the lifetime of a path. 



### -field PathMtu

Type: <b>ULONG</b>

The maximum transmission unit (MTU) size, in bytes, to the destination IP address for this IP path entry. 


### -field RttMean

Type: <b>ULONG</b>

The estimated mean round-trip time (RTT), in milliseconds, to the destination IP address for this IP path entry. 


### -field RttDeviation

Type: <b>ULONG</b>

The estimated mean deviation for the round-trip time (RTT), in milliseconds, to the destination IP address for this IP path entry. 


### -field LastReachable

Type: <b>ULONG</b>

The time, in
                     milliseconds, that a node assumes the  destination IP address is
                     reachable after having received a reachability
                     confirmation. 


### -field LastUnreachable

Type: <b>ULONG</b>

The time, in
                     milliseconds, that a node assumes the destination IP address is
                     unreachable after not having received a reachability
                     confirmation. 


### -field IsReachable

Type: <b>BOOLEAN</b>

A value that indicates if the destination IP address is reachable for this IP path entry.


### -field LinkTransmitSpeed

Type: <b>ULONG64</b>

The estimated speed in bits per second of the transmit link to the destination IP address for this IP path entry. 



### -field LinkReceiveSpeed

Type: <b>ULONG64</b>

The estimated speed in bits per second of the receive link from the destination IP address for this IP path entry. 



## -remarks



The <b>MIB_IPPATH_ROW</b> structure is defined on Windows Vista and later. 

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff552559">GetIpPathTable</a> function enumerates the IP path entries on a local system and returns this information in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff559273">MIB_IPPATH_TABLE</a> structure as an array of <b>MIB_IPPATH_ROW</b> entries. 



The <a href="https://msdn.microsoft.com/library/windows/hardware/ff552556">GetIpPathEntry</a> function retrieves a single IP path entry and returns this information in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff559273">MIB_IPPATH_TABLE</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550031">FlushIpPathTable</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552556">GetIpPathEntry</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552559">GetIpPathTable</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559273">MIB_IPPATH_TABLE</a>



<a href="https://msdn.microsoft.com/7278dcb4-65c6-4aea-a474-cb7fae4d7672">SOCKADDR_INET</a>
 

 

