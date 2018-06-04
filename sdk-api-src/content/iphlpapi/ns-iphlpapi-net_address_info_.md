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

# NET_ADDRESS_INFO_ structure


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

An IPv4 address represented as a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570823">SOCKADDR_IN</a> structure.


### -field Ipv6Address

Type: <b>SOCKADDR_IN6</b>

An IPv6 address represented as a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570824">SOCKADDR_IN6</a> structure.


### -field IpAddress

Type: <b>SOCKADDR</b>

An IPv4 or IPv6 address represented as a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">SOCKADDR</a> structure.


## -remarks



The <b>NET_ADDRESS_INFO</b> structure is defined on Windows Vista and later. 

The <b>NET_ADDRESS_INFO</b> structure is returned by the <a href="https://msdn.microsoft.com/43bc866f-7776-4f59-9ed6-4c6fc4da7f83">ParseNetworkString</a> function. 

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff570823">SOCKADDR_IN</a>,  SOCKADDR_IN6, and  SOCKADDR structures are used in the <b>NET_ADDRESS_INFO</b> structure. The SOCKADDR_IN and SOCKADDR structures are defined in the  <i>Ws2def.h</i> header file which is automatically included by the <i>Winsock2.h</i> header file. The SOCKADDR_IN6 structure is defined in the <i>Ws2ipdef.h</i> header file which is automatically included by the <i>Ws2tcpip.h</i> header file. In order to use the <b>NET_ADDRESS_INFO</b> structure, the <i>Winsock2.h</i> and <i>Ws2tcpip.h</i> header files must be included before the <i>Iphlpapi.h</i> header file.  




## -see-also




<a href="https://msdn.microsoft.com/a99df758-d46e-452d-acf8-d2cb5a6fa22e">NET_ADDRESS_FORMAT</a>



<a href="https://msdn.microsoft.com/43bc866f-7776-4f59-9ed6-4c6fc4da7f83">ParseNetworkString</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">SOCKADDR</a>
 

 

