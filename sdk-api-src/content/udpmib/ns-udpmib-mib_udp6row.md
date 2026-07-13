---
UID: NS:udpmib._MIB_UDP6ROW
title: MIB_UDP6ROW (udpmib.h)
description: Contains an entry from the User Datagram Protocol (UDP) listener table for IPv6 on the local computer.
helpviewer_keywords: ["*PMIB_UDP6ROW","MIB_UDP6ROW","MIB_UDP6ROW structure [MIB]","PMIB_UDP6ROW","PMIB_UDP6ROW structure pointer [MIB]","mib.mib_udp6row","udpmib/MIB_UDP6ROW","udpmib/PMIB_UDP6ROW"]
old-location: mib\mib_udp6row.htm
tech.root: MIB
ms.assetid: c2cc4f77-8557-4206-9e46-aadf065eb8df
ms.date: 12/05/2018
ms.keywords: '*PMIB_UDP6ROW, MIB_UDP6ROW, MIB_UDP6ROW structure [MIB], PMIB_UDP6ROW, PMIB_UDP6ROW structure pointer [MIB], mib.mib_udp6row, udpmib/MIB_UDP6ROW, udpmib/PMIB_UDP6ROW'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MIB_UDP6ROW, *PMIB_UDP6ROW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_UDP6ROW
 - udpmib/_MIB_UDP6ROW
 - PMIB_UDP6ROW
 - udpmib/PMIB_UDP6ROW
 - MIB_UDP6ROW
 - udpmib/MIB_UDP6ROW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Udpmib.h
api_name:
 - MIB_UDP6ROW
---

# MIB_UDP6ROW structure


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

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudp6table">GetUdp6Table</a> function retrieves the UDP listener table for IPv6 on the local computer and returns this information in a <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6table">MIB_UDP6TABLE</a> structure. 

An array of <b>MIB_UDP6ROW</b> structures are contained in the <b>MIB_UDP6TABLE</b> structure.  

The <b>dwLocalAddr</b> member is stored in  an <a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">in6_addr</a> structure. The <a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa">RtlIpv6AddressToString</a> or <a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw">RtlIpv6AddressToStringEx</a> functions may be used to convert the IPv6 address in the <b>dwLocalAddr</b> member to a string without loading the Windows Sockets DLL. 

The <b>dwLocalScopeId</b> and <b>dwLocalPort</b> members are in network byte order. In order to use the <b>dwLocalScopeId</b> and <b>dwLocalPort</b> members, the <a href="/windows/desktop/api/winsock/nf-winsock-ntohs">ntohs</a> or <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a> functions in Windows Sockets or similar functions may be needed. 

The <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6table">MIB_UDP6TABLE</a> structure contains the UDP listener table for IPv6 on the local computer. The name is based on the definition of this table in RFC 2454 published by the IETF. For more information, see 
<a href="http://tools.ietf.org/html/rfc2454">http://www.ietf.org/rfc/rfc2454.txt</a>. This table contains UDP  endpoints for IPv6 that have been bound to an address. It should be noted that an application can create a UDP socket and bind it to an address for the sole purpose of sending a UDP datagram, with no intention of receiving packets using this socket (functioning as a listener).

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudp6table">GetUdp6Table</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudptable">GetUdpTable</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6table">MIB_UDP6TABLE</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udprow">MIB_UDPROW</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable">MIB_UDPTABLE</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa">RtlIpv6AddressToString</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw">RtlIpv6AddressToStringEx</a>



<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">in6_addr</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a>



<a href="/windows/desktop/api/winsock/nf-winsock-ntohl">ntohl</a>



<a href="/windows/desktop/api/winsock/nf-winsock-ntohs">ntohs</a>