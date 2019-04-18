---
UID: NS:iphlpapi.NET_ADDRESS_INFO_
title: NET_ADDRESS_INFO (iphlpapi.h)
author: windows-sdk-content
description: Contains IP address information returned by the ParseNetworkString function.
old-location: iphlp\net_address_info.htm
tech.root: IpHlp
ms.assetid: 1a59cc13-a3fc-4489-aafd-444a96d9a339
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PNET_ADDRESS_INFO, NET_ADDRESS_INFO, NET_ADDRESS_INFO structure [IP Helper], NET_ADDRESS_INFO_, PNET_ADDRESS_INFO, PNET_ADDRESS_INFO structure pointer [IP Helper], iphlp.net_address_info, iphlpapi/NET_ADDRESS_INFO, iphlpapi/PNET_ADDRESS_INFO"
ms.topic: struct
req.header: iphlpapi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iphlpapi.h
api_name:
 - NET_ADDRESS_INFO
product: Windows
targetos: Windows
req.typenames: NET_ADDRESS_INFO, *PNET_ADDRESS_INFO
req.redist: 
ms.custom: 19H1
---

# NET_ADDRESS_INFO structure


## -description


The <b>NET_ADDRESS_INFO</b> structure contains IP address information returned by the <a href="https://msdn.microsoft.com/43bc866f-7776-4f59-9ed6-4c6fc4da7f83">ParseNetworkString</a> function.


## -struct-fields




### -field Format

Type: <b>NET_ADDRESS_FORMAT</b>

The format of the network address in the union in this structure. This member is an enumeration value from the <a href="https://msdn.microsoft.com/a99df758-d46e-452d-acf8-d2cb5a6fa22e">NET_ADDRESS_FORMAT</a> enumeration declared in the <i>Iphlpapi.h</i> header file.


### -field NamedAddress

A DNS named address and port.


### -field NamedAddress.Address

<b>Type: <b>WCHAR[DNS_MAX_NAME_BUFFER_LENGTH]</b>
</b>
A DNS name formatted as a <b>NULL</b>-terminated wide character string. The maximum length of this string is the <b>DNS_MAX_NAME_BUFFER_LENGTH</b> constant defined in the <i>Windns.h</i> header file.


### -field NamedAddress.Port

<b>Type: <b>WCHAR[6]</b>
</b>
The network port formatted as a <b>NULL</b>-terminated wide character string. 


### -field Ipv4Address

Type: <b>SOCKADDR_IN</b>

An IPv4 address represented as a <a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">SOCKADDR_IN</a> structure.


### -field Ipv6Address

Type: <b>SOCKADDR_IN6</b>

An IPv6 address represented as a <a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">SOCKADDR_IN6</a> structure.


### -field IpAddress

Type: <b>SOCKADDR</b>

An IPv4 or IPv6 address represented as a <a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">SOCKADDR</a> structure.


## -remarks



The <b>NET_ADDRESS_INFO</b> structure is defined on Windows Vista and later. 

The <b>NET_ADDRESS_INFO</b> structure is returned by the <a href="https://msdn.microsoft.com/43bc866f-7776-4f59-9ed6-4c6fc4da7f83">ParseNetworkString</a> function. 

The <a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">SOCKADDR_IN</a>,  SOCKADDR_IN6, and  SOCKADDR structures are used in the <b>NET_ADDRESS_INFO</b> structure. The SOCKADDR_IN and SOCKADDR structures are defined in the  <i>Ws2def.h</i> header file which is automatically included by the <i>Winsock2.h</i> header file. The SOCKADDR_IN6 structure is defined in the <i>Ws2ipdef.h</i> header file which is automatically included by the <i>Ws2tcpip.h</i> header file. In order to use the <b>NET_ADDRESS_INFO</b> structure, the <i>Winsock2.h</i> and <i>Ws2tcpip.h</i> header files must be included before the <i>Iphlpapi.h</i> header file.  




## -see-also




<a href="https://msdn.microsoft.com/a99df758-d46e-452d-acf8-d2cb5a6fa22e">NET_ADDRESS_FORMAT</a>



<a href="https://msdn.microsoft.com/43bc866f-7776-4f59-9ed6-4c6fc4da7f83">ParseNetworkString</a>



<a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">SOCKADDR</a>
 

 

