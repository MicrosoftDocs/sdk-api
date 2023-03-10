---
UID: NS:udpmib._MIB_UDPROW
title: MIB_UDPROW (udpmib.h)
description: Contains an entry from the User Datagram Protocol (UDP) listener table for IPv4 on the local computer.
helpviewer_keywords: ["*PMIB_UDPROW","MIB_UDPROW","MIB_UDPROW structure [MIB]","PMIB_UDPROW","PMIB_UDPROW structure pointer [MIB]","_mpr_mib_udprow","iprtrmib/MIB_UDPROW","iprtrmib/PMIB_UDPROW","mib.mib_udprow","rras.mib_udprow","udpmib/MIB_UDPROW","udpmib/PMIB_UDPROW"]
old-location: mib\mib_udprow.htm
tech.root: MIB
ms.assetid: db366802-962f-4e83-838e-1e2f51beab92
ms.date: 12/05/2018
ms.keywords: '*PMIB_UDPROW, MIB_UDPROW, MIB_UDPROW structure [MIB], PMIB_UDPROW, PMIB_UDPROW structure pointer [MIB], _mpr_mib_udprow, iprtrmib/MIB_UDPROW, iprtrmib/PMIB_UDPROW, mib.mib_udprow, rras.mib_udprow, udpmib/MIB_UDPROW, udpmib/PMIB_UDPROW'
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
targetos: Windows
req.typenames: MIB_UDPROW, *PMIB_UDPROW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_UDPROW
 - udpmib/_MIB_UDPROW
 - PMIB_UDPROW
 - udpmib/PMIB_UDPROW
 - MIB_UDPROW
 - udpmib/MIB_UDPROW
dev_langs:
 - c++
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

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudptable">GetUdpTable</a> function retrieves the IPv4 UDP listener table on the local computer and returns this information in a <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable">MIB_UDPTABLE</a> structure. 

An array of <b>MIB_UDPROW</b> structures are contained in the <b>MIB_UDPTABLE</b> structure.  

The <b>dwLocalAddr</b> member is stored as a <b>DWORD</b> in the same format as the  <a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">in_addr</a> structure. In order to use the <b>dwLocalAddr</b> member, the <a href="/windows/desktop/api/winsock/nf-winsock-ntohl">ntohl</a> or <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a> functions in Windows Sockets or similar functions may be needed. On Windows Vista and later, the <a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa">RtlIpv4AddressToString</a> or <a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringexw">RtlIpv4AddressToStringEx</a> functions may be used to convert the IPv4 address in the <b>dwLocalAddr</b>  member to a string without loading the Windows Sockets DLL. 

The <b>dwLocalPort</b> member is in network byte order. In order to use the <b>dwLocalPort</b> member, the <a href="/windows/desktop/api/winsock/nf-winsock-ntohs">ntohs</a> or <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a> functions in Windows Sockets or similar functions may be needed. 

The <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable">MIB_UDPTABLE</a> structure contains the UDP listener table for IPv4 on the local computer. The name is based on the definition of this table in RFC 1213 published by the IETF. For more information, see 
<a href="http://tools.ietf.org/html/rfc1213">http://www.ietf.org/rfc/rfc1213.txt</a>. This table contains UDP  endpoints for IPv4 that have been bound to an address. It should be noted that an application can create a UDP socket and bind it to an address for the sole purpose of sending a UDP datagram, with no intention of receiving packets using this socket (functioning as a listener). 

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed. This  structure is defined in the <i>Udpmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Udpmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Udpmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedudptable">GetExtendedUdpTable</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudp6table">GetUdp6Table</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudptable">GetUdpTable</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6row">MIB_UDP6ROW</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6table">MIB_UDP6TABLE</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udpstats">MIB_UDPSTATS</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable">MIB_UDPTABLE</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa">RtlIpv4AddressToString</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringexw">RtlIpv4AddressToStringEx</a>



<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">in_addr</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a>



<a href="/windows/desktop/api/winsock/nf-winsock-ntohl">ntohl</a>



<a href="/windows/desktop/api/winsock/nf-winsock-ntohs">ntohs</a>