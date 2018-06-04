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

# _MIB_MULTICASTIPADDRESS_ROW structure


## -description


The 
<b>MIB_MULTICASTIPADDRESS_ROW</b> structure stores information about a  multicast IP address.


## -struct-fields




### -field Address

The multicast IP address. This member can be an IPv6 address or an IPv4 address.


### -field InterfaceIndex

The local index value for the network interface associated with this IP address. This index value may change when a network adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent. 


### -field InterfaceLuid

The locally unique identifier (LUID) for the network interface associated with this IP address.


### -field ScopeId

The scope ID of the multicast IP address. This member is applicable only to an IPv6 address. This member cannot be set. It is automatically determined by the interface on which the address was added.

 




## -remarks



The <b>MIB_MULTICASTIPADDRESS_ROW</b> structure is defined on Windows Vista and later. 

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff552570">GetMulticastIpAddressTable</a> function enumerates the multicast IP addresses on a local system and returns this information in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff559281">MIB_MULTICASTIPADDRESS_TABLE</a> structure. The <a href="https://msdn.microsoft.com/library/windows/hardware/ff552565">GetMulticastIpAddressEntry</a> function retrieves a single multicast IP address and returns this information in a <b>MIB_MULTICASTIPADDRESS_ROW</b> structure.

Note that the <i>Netioapi.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Netioapi.h</i> header file should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552565">GetMulticastIpAddressEntry</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552570">GetMulticastIpAddressTable</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559281">MIB_MULTICASTIPADDRESS_TABLE</a>



<a href="https://msdn.microsoft.com/7278dcb4-65c6-4aea-a474-cb7fae4d7672">SOCKADDR_INET</a>
 

 

