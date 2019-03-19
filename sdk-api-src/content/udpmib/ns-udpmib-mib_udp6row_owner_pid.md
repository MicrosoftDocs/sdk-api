---
UID: NS:udpmib._MIB_UDP6ROW_OWNER_PID
title: MIB_UDP6ROW_OWNER_PID (udpmib.h)
author: windows-sdk-content
description: Contains an entry from the User Datagram Protocol (UDP) listener table for IPv6 on the local computer. The entry also includes the process ID (PID) that issued the call to the bind function for the UDP endpoint.
old-location: mib\mib_udp6row_owner_pid.htm
tech.root: MIB
ms.assetid: d3d02485-381b-4058-b4b9-0a2c9c365f43
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PMIB_UDP6ROW_OWNER_PID, MIB_UDP6ROW_OWNER_PID, MIB_UDP6ROW_OWNER_PID structure [MIB], PMIB_UDP6ROW_OWNER_PID, PMIB_UDP6ROW_OWNER_PID structure pointer [MIB], iprtrmib/MIB_UDP6ROW_OWNER_PID, iprtrmib/PMIB_UDP6ROW_OWNER_PID, mib.mib_udp6row_owner_pid, udpmib/MIB_UDP6ROW_OWNER_PID, udpmib/PMIB_UDP6ROW_OWNER_PID"
ms.topic: struct
req.header: udpmib.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
 - MIB_UDP6ROW_OWNER_PID
product: Windows
targetos: Windows
req.typenames: MIB_UDP6ROW_OWNER_PID, *PMIB_UDP6ROW_OWNER_PID
req.redist: 
---

# MIB_UDP6ROW_OWNER_PID structure


## -description


The <b>MIB_UDP6ROW_OWNER_PID</b> structure  contains an entry from the User Datagram Protocol (UDP)  listener table for IPv6 on the local computer. The entry also includes the process ID (PID) that issued the call to the <a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a> function for the UDP endpoint.


## -struct-fields




### -field ucLocalAddr

The IPv6 address for the local UDP endpoint. This member is stored in  a character array in network byte order. 

A value of zero indicates a UDP listener  willing to accept datagrams for any IP interface associated
                      with the local computer.


### -field dwLocalScopeId

The scope ID for the IPv6 address of the UDP endpoint on the local computer. This member is stored in network byte order.


### -field dwLocalPort

The port number of the UDP endpoint on the local computer. This member is stored in network byte order.


### -field dwOwningPid

The PID of the process that issued a context bind for this endpoint. If this value is set to 0, the information for this endpoint is unavailable.


## -remarks



The <a href="https://msdn.microsoft.com/6c8d1cb9-209b-47a0-b41c-6b4098a4a81e">MIB_UDP6TABLE_OWNER_PID</a> structure is returned by a call to <a href="https://msdn.microsoft.com/c936d5a0-ca5e-487e-b304-bfd81403ab40">GetExtendedUdpTable</a> with the <i>TableClass</i> parameter set to a  <b>UDP_TABLE_OWNER_PID</b> from the <a href="https://msdn.microsoft.com/2e7304d1-b89c-46d4-9121-936a1c38cc51">UDP_TABLE_CLASS</a> enumeration and the <i>ulAf</i> parameter set to <b>AF_INET6</b>. The <b>MIB_UDP6TABLE_OWNER_PID</b> structure contains an array of <b>MIB_UDP6ROW_OWNER_PID</b> structures.

The <b>ucLocalAddr</b> member is stored in  a character array in network byte order. On Windows Vistaand later, the <a href="https://msdn.microsoft.com/a891adb0-6c2d-4b69-a0de-4a615be938e3">RtlIpv6AddressToString</a> or <a href="https://msdn.microsoft.com/a7de2da3-21ea-42fa-9474-f33252838632">RtlIpv6AddressToStringEx</a> functions may be used to convert the IPv6 address in the <b>ucLocalAddr</b> member to a string without loading the Windows Sockets DLL. 

The <b>dwLocalScopeId</b> member is in network byte order. In order to use the <b>dwLocalScopeId</b> member, the <a href="https://msdn.microsoft.com/04673bef-22c6-424f-a5ae-689fb648b54e">ntohl</a> or <a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a> functions in Windows Sockets or similar functions may be needed. 

The <b>dwLocalPort</b> member are in network byte order. In order to use the <b>dwLocalPort</b> member, the <a href="https://msdn.microsoft.com/9946df13-3b40-4bcb-91ca-10684b3fc9a5">ntohs</a> or <a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a> functions in Windows Sockets or similar functions may be needed. 

The <a href="https://msdn.microsoft.com/6c8d1cb9-209b-47a0-b41c-6b4098a4a81e">MIB_UDP6TABLE_OWNER_PID</a> structure contains the UDP listener table for IPv6 on the local computer. The name is based on the definition of this table in RFC 2454 published by the IETF. For more information, see 
<a href="http://go.microsoft.com/fwlink/p/?linkid=85985">http://www.ietf.org/rfc/rfc2454.txt</a>. This table contains UDP  endpoints for IPv6 that have been bound to an address. It should be noted that an application can create a UDP socket and bind it to an address for the sole purpose of sending a UDP datagram, with no intention of receiving packets using this socket (functioning as a listener). 

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vistaand later, the organization of header files has changed. This  structure is defined in the <i>Udpmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Udpmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Udpmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/c936d5a0-ca5e-487e-b304-bfd81403ab40">GetExtendedUdpTable</a>



<a href="https://msdn.microsoft.com/6c8d1cb9-209b-47a0-b41c-6b4098a4a81e">MIB_UDP6TABLE_OWNER_PID</a>



<a href="https://msdn.microsoft.com/a891adb0-6c2d-4b69-a0de-4a615be938e3">RtlIpv6AddressToString</a>



<a href="https://msdn.microsoft.com/a7de2da3-21ea-42fa-9474-f33252838632">RtlIpv6AddressToStringEx</a>



<a href="https://msdn.microsoft.com/2e7304d1-b89c-46d4-9121-936a1c38cc51">UDP_TABLE_CLASS</a>



<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>



<a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a>



<a href="https://msdn.microsoft.com/04673bef-22c6-424f-a5ae-689fb648b54e">ntohl</a>



<a href="https://msdn.microsoft.com/9946df13-3b40-4bcb-91ca-10684b3fc9a5">ntohs</a>
 

 

