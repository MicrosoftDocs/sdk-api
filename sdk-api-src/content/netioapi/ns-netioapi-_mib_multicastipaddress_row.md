---
UID: NS:netioapi._MIB_MULTICASTIPADDRESS_ROW
title: "_MIB_MULTICASTIPADDRESS_ROW"
author: windows-sdk-content
description: Stores information about a multicast IP address.
old-location: mib\mib_multicastipaddress_row.htm
old-project: MIB
ms.assetid: 2b75d1bd-2867-43e1-94e6-626fc761dac6
ms.author: windowssdkdev
ms.date: 05/14/2018
ms.keywords: "*PMIB_MULTICASTIPADDRESS_ROW, MIB_MULTICASTIPADDRESS_ROW, MIB_MULTICASTIPADDRESS_ROW structure [MIB], PMIB_MULTICASTIPADDRESS_ROW, PMIB_MULTICASTIPADDRESS_ROW structure pointer [MIB], _MIB_MULTICASTIPADDRESS_ROW, mib.mib_multicastipaddress_row, netioapi/MIB_MULTICASTIPADDRESS_ROW, netioapi/PMIB_MULTICASTIPADDRESS_ROW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MIB_MULTICASTIPADDRESS_ROW, *PMIB_MULTICASTIPADDRESS_ROW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Netioapi.h
api_name:
-	MIB_MULTICASTIPADDRESS_ROW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

