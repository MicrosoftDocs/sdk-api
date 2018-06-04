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

# _SOCKADDR_INET structure


## -description


The <b>SOCKADDR_INET</b> union contains an IPv4, an IPv6 address, or an address family.


## -struct-fields




### -field Ipv4

Type: <b>SOCKADDR_IN</b>

An IPv4 address represented as a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570823">SOCKADDR_IN</a> structure containing the address family and the IPv4 address. The address family is in host byte order and the IPv4 address is  in network byte order.

On the Windows SDK released for Windows Vista and later, the organization of header files has changed and the <a href="https://msdn.microsoft.com/library/windows/hardware/ff570823">SOCKADDR_IN</a> structure is defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.


### -field Ipv6

Type: <b>SOCKADDR_IN6</b>

An IPv6 address represented as a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570824">SOCKADDR_IN6</a> structure containing the address family and the IPv6 address. The address family is in host byte order and the IPv6 address is  in network byte order.

On the Windows SDK released for Windows Vista and later, the organization of header files has changed and the <a href="https://msdn.microsoft.com/library/windows/hardware/ff570824">SOCKADDR_IN6</a> structure is defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.


### -field si_family

Type: <b>ADDRESS_FAMILY</b>

The address family. 

Possible values for the address family are listed in the <i>Ws2def.h</i> header file. Note that the values for the AF_ address family and PF_ protocol family constants  are identical (for example, <b>AF_INET</b> and <b>PF_INET</b>), so either constant can be used. The <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly. 

The values currently supported are <b>AF_INET</b>, <b>AF_INET6</b>, and <b>AF_UNSPEC</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AF_UNSPEC"></a><a id="af_unspec"></a><dl>
<dt><b>AF_UNSPEC</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The address family is unspecified. When this parameter is specified,  the <b>SOCKADDR_INET</b> union can represent either the IPv4 or IPv6 address family. 

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET"></a><a id="af_inet"></a><dl>
<dt><b>AF_INET</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 4 (IPv4) address family. 

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
<dt>23</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 6 (IPv6) address family. 

</td>
</tr>
</table>
 


## -remarks



The <b>SOCKADDR_INET</b> union is defined on Windows Vista and later. 

The <b>SOCKADDR_INET</b> union is a convenience structure for accessing an IPv4 address, an IPv6 address, or the IP address family without having to cast  the <a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a> structure.

The <b>SOCKADDR_INET</b> union is the data type of the <b>Prefix</b> member in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff557013">IP_ADDRESS_PREFIX</a> structure  

Note that the <i>Ws2ipdef.h</i> header file is automatically included in <i>Ws2tcpip.h</i> header file, and should never be used directly.





## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff557013">IP_ADDRESS_PREFIX</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a>
 

 

