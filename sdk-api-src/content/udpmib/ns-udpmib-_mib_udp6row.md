---
UID: NS:udpmib._MIB_UDP6ROW
title: "_MIB_UDP6ROW"
author: windows-sdk-content
description: Contains an entry from the User Datagram Protocol (UDP) listener table for IPv6 on the local computer.
old-location: mib\mib_udp6row.htm
old-project: MIB
ms.assetid: c2cc4f77-8557-4206-9e46-aadf065eb8df
ms.author: windowssdkdev
ms.date: 05/14/2018
ms.keywords: "*PMIB_UDP6ROW, MIB_UDP6ROW, MIB_UDP6ROW structure [MIB], PMIB_UDP6ROW, PMIB_UDP6ROW structure pointer [MIB], _MIB_UDP6ROW, mib.mib_udp6row, udpmib/MIB_UDP6ROW, udpmib/PMIB_UDP6ROW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: udpmib.h
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
req.typenames: MIB_UDP6ROW, *PMIB_UDP6ROW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Udpmib.h
api_name:
-	MIB_UDP6ROW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _MIB_UDP6ROW structure


## -description


The 
<b>MIB_UDP6ROW</b> structure contains an entry from the User Datagram Protocol (UDP) listener table for IPv6 on the local computer. 


## -struct-fields




### -field dwLocalAddr

The IPv6 address of the UDP endpoint on the local computer. This member is stored in  a character array in network byte order. 

A value of zero indicates a UDP listener  willing to accept datagrams for any IP interface associated
                      with the local computer.


### -field dwLocalScopeId

The scope ID for the IPv6 address of the UDP endpoint on the local computer. This member is stored in network byte order.


### -field dwLocalPort

The port number of the UDP endpoint on the local computer. This member is stored in network byte order.


## -remarks



The <b>MIB_UDP6ROW</b> structure is defined on Windows Vista and later. 

The <a href="https://msdn.microsoft.com/5e86483c-aa39-4d6c-a9b4-9b046b3dcc74">GetUdp6Table</a>
			function retrieves the UDP listener table for IPv6 on the local computer and returns this information in a <a href="https://msdn.microsoft.com/49da9a1f-f244-464e-96b2-944a286445d4">MIB_UDP6TABLE</a> structure. 

An array of <b>MIB_UDP6ROW</b> structures are contained in the <b>MIB_UDP6TABLE</b> structure.  

The <b>dwLocalAddr</b> member is stored in  an <a href="https://msdn.microsoft.com/library/windows/hardware/ff554787">in6_addr</a> structure. The <a href="https://msdn.microsoft.com/a891adb0-6c2d-4b69-a0de-4a615be938e3">RtlIpv6AddressToString</a> or <a href="https://msdn.microsoft.com/a7de2da3-21ea-42fa-9474-f33252838632">RtlIpv6AddressToStringEx</a> functions may be used to convert the IPv6 address in the <b>dwLocalAddr</b> member to a string without loading the Windows Sockets DLL. 

The <b>dwLocalScopeId</b> and <b>dwLocalPort</b> members are in network byte order. In order to use the <b>dwLocalScopeId</b> and <b>dwLocalPort</b> members, the <a href="https://msdn.microsoft.com/9946df13-3b40-4bcb-91ca-10684b3fc9a5">ntohs</a> or <a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a> functions in Windows Sockets or similar functions may be needed. 

The <a href="https://msdn.microsoft.com/49da9a1f-f244-464e-96b2-944a286445d4">MIB_UDP6TABLE</a> structure contains the UDP listener table for IPv6 on the local computer. The name is based on the definition of this table in RFC 2454 published by the IETF. For more information, see 
<a href="http://go.microsoft.com/fwlink/p/?linkid=85985">http://www.ietf.org/rfc/rfc2454.txt</a>. This table contains UDP  endpoints for IPv6 that have been bound to an address. It should be noted that an application can create a UDP socket and bind it to an address for the sole purpose of sending a UDP datagram, with no intention of receiving packets using this socket (functioning as a listener). 




## -see-also




<a href="https://msdn.microsoft.com/5e86483c-aa39-4d6c-a9b4-9b046b3dcc74">GetUdp6Table</a>



<a href="https://msdn.microsoft.com/00e80e90-1a6d-426d-90cd-20b967ebbb8e">GetUdpTable</a>



<a href="https://msdn.microsoft.com/49da9a1f-f244-464e-96b2-944a286445d4">MIB_UDP6TABLE</a>



<a href="https://msdn.microsoft.com/db366802-962f-4e83-838e-1e2f51beab92">MIB_UDPROW</a>



<a href="https://msdn.microsoft.com/83608d38-e352-483a-b284-2f9cb444e64f">MIB_UDPTABLE</a>



<a href="https://msdn.microsoft.com/a891adb0-6c2d-4b69-a0de-4a615be938e3">RtlIpv6AddressToString</a>



<a href="https://msdn.microsoft.com/a7de2da3-21ea-42fa-9474-f33252838632">RtlIpv6AddressToStringEx</a>



<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff554787">in6_addr</a>



<a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a>



<a href="https://msdn.microsoft.com/04673bef-22c6-424f-a5ae-689fb648b54e">ntohl</a>



<a href="https://msdn.microsoft.com/9946df13-3b40-4bcb-91ca-10684b3fc9a5">ntohs</a>
 

 

