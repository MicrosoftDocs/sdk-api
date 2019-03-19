---
UID: NS:udpmib._MIB_UDPROW
title: MIB_UDPROW (udpmib.h)
author: windows-sdk-content
description: Contains an entry from the User Datagram Protocol (UDP) listener table for IPv4 on the local computer.
old-location: mib\mib_udprow.htm
tech.root: MIB
ms.assetid: db366802-962f-4e83-838e-1e2f51beab92
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PMIB_UDPROW, MIB_UDPROW, MIB_UDPROW structure [MIB], PMIB_UDPROW, PMIB_UDPROW structure pointer [MIB], _mpr_mib_udprow, iprtrmib/MIB_UDPROW, iprtrmib/PMIB_UDPROW, mib.mib_udprow, rras.mib_udprow, udpmib/MIB_UDPROW, udpmib/PMIB_UDPROW"
ms.topic: struct
req.header: udpmib.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Udpmib.h
 - Iprtrmib.h
api_name:
 - MIB_UDPROW
product: Windows
targetos: Windows
req.typenames: MIB_UDPROW, *PMIB_UDPROW
req.redist: 
---

# MIB_UDPROW structure


## -description


The 
<b>MIB_UDPROW</b> structure contains an entry from the User Datagram Protocol (UDP)  listener table for IPv4 on the local computer. 


## -struct-fields




### -field dwLocalAddr

The IPv4 address of the UDP endpoint on the local computer. 

A value of zero indicates a UDP listener  willing to accept datagrams for any IP interface associated
                      with the local computer.


### -field dwLocalPort

The port number of the UDP endpoint on the local computer. This member is stored in network byte order.


## -remarks



The <a href="https://msdn.microsoft.com/en-us/library/Aa366033(v=VS.85).aspx">GetUdpTable</a>function retrieves the IPv4 UDP listener table on the local computer and returns this information in a <a href="https://msdn.microsoft.com/83608d38-e352-483a-b284-2f9cb444e64f">MIB_UDPTABLE</a> structure. 

An array of <b>MIB_UDPROW</b> structures are contained in the <b>MIB_UDPTABLE</b> structure.  

The <b>dwLocalAddr</b> member is stored as a <b>DWORD</b> in the same format as the  <a href="https://msdn.microsoft.com/fc41a2d1-ea6e-41bb-b2c8-531ac8b5434c">in_addr</a> structure. In order to use the <b>dwLocalAddr</b> member, the <a href="https://msdn.microsoft.com/04673bef-22c6-424f-a5ae-689fb648b54e">ntohl</a> or <a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a> functions in Windows Sockets or similar functions may be needed. On Windows Vistaand later, the <a href="https://msdn.microsoft.com/f198b770-9429-4b51-9fb4-06cf9917bc21">RtlIpv4AddressToString</a> or <a href="https://msdn.microsoft.com/4244eaaf-8522-4edb-abb8-dc2b063c9076">RtlIpv4AddressToStringEx</a> functions may be used to convert the IPv4 address in the <b>dwLocalAddr</b>  member to a string without loading the Windows Sockets DLL. 

The <b>dwLocalPort</b> member is in network byte order. In order to use the <b>dwLocalPort</b> member, the <a href="https://msdn.microsoft.com/9946df13-3b40-4bcb-91ca-10684b3fc9a5">ntohs</a> or <a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a> functions in Windows Sockets or similar functions may be needed. 

The <a href="https://msdn.microsoft.com/83608d38-e352-483a-b284-2f9cb444e64f">MIB_UDPTABLE</a> structure contains the UDP listener table for IPv4 on the local computer. The name is based on the definition of this table in RFC 1213 published by the IETF. For more information, see 
<a href="http://go.microsoft.com/fwlink/p/?linkid=85984">http://www.ietf.org/rfc/rfc1213.txt</a>. This table contains UDP  endpoints for IPv4 that have been bound to an address. It should be noted that an application can create a UDP socket and bind it to an address for the sole purpose of sending a UDP datagram, with no intention of receiving packets using this socket (functioning as a listener). 

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vistaand later, the organization of header files has changed. This  structure is defined in the <i>Udpmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Udpmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Udpmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/c936d5a0-ca5e-487e-b304-bfd81403ab40">GetExtendedUdpTable</a>



<a href="https://msdn.microsoft.com/5e86483c-aa39-4d6c-a9b4-9b046b3dcc74">GetUdp6Table</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa366033(v=VS.85).aspx">GetUdpTable</a>



<a href="https://msdn.microsoft.com/c2cc4f77-8557-4206-9e46-aadf065eb8df">MIB_UDP6ROW</a>



<a href="https://msdn.microsoft.com/49da9a1f-f244-464e-96b2-944a286445d4">MIB_UDP6TABLE</a>



<a href="https://msdn.microsoft.com/128bae44-59a2-4e37-a588-a18805b9e340">MIB_UDPSTATS</a>



<a href="https://msdn.microsoft.com/83608d38-e352-483a-b284-2f9cb444e64f">MIB_UDPTABLE</a>



<a href="https://msdn.microsoft.com/f198b770-9429-4b51-9fb4-06cf9917bc21">RtlIpv4AddressToString</a>



<a href="https://msdn.microsoft.com/4244eaaf-8522-4edb-abb8-dc2b063c9076">RtlIpv4AddressToStringEx</a>



<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>



<a href="https://msdn.microsoft.com/fc41a2d1-ea6e-41bb-b2c8-531ac8b5434c">in_addr</a>



<a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a>



<a href="https://msdn.microsoft.com/04673bef-22c6-424f-a5ae-689fb648b54e">ntohl</a>



<a href="https://msdn.microsoft.com/9946df13-3b40-4bcb-91ca-10684b3fc9a5">ntohs</a>
 

 

