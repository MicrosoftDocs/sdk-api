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

# _HTTP_SERVICE_CONFIG_IP_LISTEN_QUERY structure


## -description


The 
<b>HTTP_SERVICE_CONFIG_IP_LISTEN_QUERY</b> structure is used by 
<a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HttpQueryServiceConfiguration</a> to return a list of the Internet Protocol (IP) addresses to which the HTTP service binds.


## -struct-fields




### -field AddrCount

The number of address structures in the <b>AddrList</b> array.


### -field AddrList

An array of 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff570825">SOCKADDR_STORAGE</a> structures that contains IP addresses in either IPv4 or IPv6 form. To determine what form an address in the list has, cast it to a SOCKADDR and examine the <b>sa_family</b> element. If <b>sa_family</b> is equal to AF_INET, the address is in IPv4 form, or if it is equal to AF_INET6, the address is in IPv6 form.


## -remarks



An IPv4 address may be expressed as a literal string of four dotted decimal numbers, each in the range 0-255, such as 192.168.197.113. IPv4 addresses are contained in <b>sockaddr_in</b> structures, declared in the Windows header file Winsock2.h as follows:

<pre class="syntax" xml:space="preserve"><code>  struct sockaddr_in {
    short    sin_family;        /* == AF_INET */
    u_short  sin_port;          /* Transport-level port number */
    struct   in_addr sin_addr;  /* IPv4 address */
    char     sin_zero[8];
  };
</code></pre>
The <b>SOCKADDR_IN</b> structure is exactly equivalent to <b>sockaddr_in</b> by typedef.

An IPv6 address can be expressed as a literal string enclosed in square brackets that contains hex numbers separated by colons; examples are: [::1] and [3ffe:ffff:6ECB:0101]. IPv6 addresses are contained in <b>sockaddr_in6</b> structures, declared in the Windows header file WS2tcpip.h as follows:

<pre class="syntax" xml:space="preserve"><code>  struct sockaddr_in6 {
    short    sin6_family;       /* == AF_INET6 */
    u_short  sin6_port;         /* Transport-level port number */
    u_long   sin6_flowinfo;     /* IPv6 flow information */
    IN6_ADDR sin6_addr;         /* IPv6 address */
    u_long   sin6_scope_id;     /* set of scope interfaces */
  };
</code></pre>
The <b>SOCKADDR_IN6</b> structure is exactly equivalent to <b>sockaddr_in6</b> by typedef.




## -see-also




<a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HttpQueryServiceConfiguration</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570825">SOCKADDR_STORAGE</a>
 

 

