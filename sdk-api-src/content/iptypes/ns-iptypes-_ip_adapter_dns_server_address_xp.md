---
UID: NS:iptypes._IP_ADAPTER_DNS_SERVER_ADDRESS_XP
title: "_IP_ADAPTER_DNS_SERVER_ADDRESS_XP"
author: windows-driver-content
description: The IP_ADAPTER_DNS_SERVER_ADDRESS structure stores a single DNS server address in a linked list of DNS server addresses for a particular adapter.
old-location: iphlp\ip_adapter_dns_server_address.htm
old-project: IpHlp
ms.assetid: 96855386-9010-40df-8260-16b43ad6646f
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: "*PIP_ADAPTER_DNS_SERVER_ADDRESS, *PIP_ADAPTER_DNS_SERVER_ADDRESS_XP, IP_ADAPTER_DNS_SERVER_ADDRESS, IP_ADAPTER_DNS_SERVER_ADDRESS structure [IP Helper], IP_ADAPTER_DNS_SERVER_ADDRESS_XP, PIP_ADAPTER_DNS_SERVER_ADDRESS, PIP_ADAPTER_DNS_SERVER_ADDRESS structure pointer [IP Helper], _IP_ADAPTER_DNS_SERVER_ADDRESS_XP, _iphlp_ip_adapter_dns_server_address, iphlp.ip_adapter_dns_server_address, iptypes/IP_ADAPTER_DNS_SERVER_ADDRESS, iptypes/PIP_ADAPTER_DNS_SERVER_ADDRESS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: iptypes.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IP_ADAPTER_DNS_SERVER_ADDRESS_XP, *PIP_ADAPTER_DNS_SERVER_ADDRESS_XP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Iptypes.h
api_name:
-	IP_ADAPTER_DNS_SERVER_ADDRESS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _IP_ADAPTER_DNS_SERVER_ADDRESS_XP structure


## -description


The 
<b>IP_ADAPTER_DNS_SERVER_ADDRESS</b> structure stores a single DNS server address in a linked list of DNS server addresses for a particular adapter.


## -struct-fields




### -field Length

The length, in bytes, of this structure.


### -field Reserved

Reserved. 
							


### -field Next

A pointer to the next DNS server address structure in the list.


### -field Address

The IP address for this DNS server entry. This member can be an IPv6 address or an IPv4 address. 


#### - Alignment

Reserved. Used by the compiler to align the structure.


## -remarks



The <a href="https://msdn.microsoft.com/a2df3749-6c75-40c0-8952-1656bbe639a6">IP_ADAPTER_ADDRESSES</a> structure is retrieved by the <a href="https://msdn.microsoft.com/7b34138f-7263-4b73-95df-9e854fd81135">GetAdaptersAddresses</a> function. The <b>FirstDnsServerAddress</b> member of the <b>IP_ADAPTER_ADDRESSES</b>
		structure is a pointer to a linked list of <b>IP_ADAPTER_DNS_SERVER_ADDRESS</b> structures. 

The <a href="https://msdn.microsoft.com/37fbcb96-a859-4eca-8928-8051f95407b9">SOCKET_ADDRESS</a> structure is used in the <b>IP_ADAPTER_DNS_SERVER_ADDRESS</b> structure. On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>SOCKET_ADDRESS</b> structure is defined in the <i>Ws2def.h</i> header file which is automatically included by the <i>Winsock2.h</i> header file. On the Platform Software Development Kit (SDK) released for Windows Server 2003 and Windows XP, the <b>SOCKET_ADDRESS</b> structure is declared in the <i>Winsock2.h</i> header file. In order to use the <b>IP_ADAPTER_DNS_SERVER_ADDRESS</b> structure, the <i>Winsock2.h</i> header file must be included before the <i>Iphlpapi.h</i> header file.  




## -see-also




<a href="https://msdn.microsoft.com/7b34138f-7263-4b73-95df-9e854fd81135">GetAdaptersAddresses</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/d53c3821-00a0-4eaa-9a06-69ec7aa98d84">IP Helper Structures</a>



<a href="https://msdn.microsoft.com/a2df3749-6c75-40c0-8952-1656bbe639a6">IP_ADAPTER_ADDRESSES</a>



<a href="https://msdn.microsoft.com/37fbcb96-a859-4eca-8928-8051f95407b9">SOCKET_ADDRESS</a>
 

 

