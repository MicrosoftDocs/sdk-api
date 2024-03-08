---
UID: NS:udpmib._MIB_UDP6ROW_OWNER_MODULE
title: MIB_UDP6ROW_OWNER_MODULE (udpmib.h)
description: Contains an entry from the User Datagram Protocol (UDP) listener table for IPv6 on the local computer. This entry also includes any available ownership data and the process ID (PID) that issued the call to the bind function for the UDP endpoint.
helpviewer_keywords: ["*PMIB_UDP6ROW_OWNER_MODULE","MIB_UDP6ROW_OWNER_MODULE","MIB_UDP6ROW_OWNER_MODULE structure [MIB]","PMIB_UDP6ROW_OWNER_MODULE","PMIB_UDP6ROW_OWNER_MODULE structure pointer [MIB]","iprtrmib/MIB_UDP6ROW_OWNER_MODULE","iprtrmib/PMIB_UDP6ROW_OWNER_MODULE","mib.mib_udp6row_owner_module","udpmib/MIB_UDP6ROW_OWNER_MODULE","udpmib/PMIB_UDP6ROW_OWNER_MODULE"]
old-location: mib\mib_udp6row_owner_module.htm
tech.root: MIB
ms.assetid: dcc80b3c-d4d5-44f4-9c7f-df6be2e21889
ms.date: 12/05/2018
ms.keywords: '*PMIB_UDP6ROW_OWNER_MODULE, MIB_UDP6ROW_OWNER_MODULE, MIB_UDP6ROW_OWNER_MODULE structure [MIB], PMIB_UDP6ROW_OWNER_MODULE, PMIB_UDP6ROW_OWNER_MODULE structure pointer [MIB], iprtrmib/MIB_UDP6ROW_OWNER_MODULE, iprtrmib/PMIB_UDP6ROW_OWNER_MODULE, mib.mib_udp6row_owner_module, udpmib/MIB_UDP6ROW_OWNER_MODULE, udpmib/PMIB_UDP6ROW_OWNER_MODULE'
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
targetos: Windows
req.typenames: MIB_UDP6ROW_OWNER_MODULE, *PMIB_UDP6ROW_OWNER_MODULE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_UDP6ROW_OWNER_MODULE
 - udpmib/_MIB_UDP6ROW_OWNER_MODULE
 - PMIB_UDP6ROW_OWNER_MODULE
 - udpmib/PMIB_UDP6ROW_OWNER_MODULE
 - MIB_UDP6ROW_OWNER_MODULE
 - udpmib/MIB_UDP6ROW_OWNER_MODULE
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
 - MIB_UDP6ROW_OWNER_MODULE
---

# MIB_UDP6ROW_OWNER_MODULE structure


## -description

The <b>MIB_UDP6ROW_OWNER_MODULE</b> structure contains an entry from the User Datagram Protocol (UDP) listener table for IPv6 on the local computer. This entry also includes any available ownership data and the process ID (PID) that issued the call to the <a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function for the UDP endpoint.

## -struct-fields

### -field ucLocalAddr

Type: <b>UCHAR[16]</b>

The IPv6 address of the UDP endpoint on the local computer. This member is stored in  a character array in network byte order. 

A value of zero indicates a UDP listener  willing to accept datagrams for any IP interface associated
                      with the local computer.

### -field dwLocalScopeId

Type: <b>DWORD</b>

The scope ID for the IPv6 address of the UDP endpoint on the local computer.

### -field dwLocalPort

Type: <b>DWORD</b>

The port number for the local UDP endpoint.

### -field dwOwningPid

Type: <b>DWORD</b>

The PID of the process that issued a context bind for this endpoint. If this value is set to 0, the information for this endpoint is unavailable.

### -field liCreateTimestamp

Type: <b>LARGE_INTEGER</b>

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that indicates when the context bind operation that created this endpoint occurred.

### -field SpecificPortBind

Type: <b>int</b>

A value that indicates if a specific port was specified in the last context bind operation.

### -field dwFlags

Type: <b>int</b>

A set of flags. This member is not currently used.

### -field OwningModuleInfo

Type: <b>ULONGLONG[TCPIP_OWNING_MODULE_SIZE]</b>

An array of opaque data that contains ownership information.

## -remarks

The <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6table_owner_module">MIB_UDP6TABLE_OWNER_MODULE</a> structure is returned by a call to <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedudptable">GetExtendedUdpTable</a> with the <i>TableClass</i> parameter set to a  <b>UDP_TABLE_OWNER_MODULE</b> from the <a href="/windows/desktop/api/iprtrmib/ne-iprtrmib-udp_table_class">UDP_TABLE_CLASS</a> enumeration and the <i>ulAf</i> parameter set to <b>AF_INET6</b>. The <b>MIB_UDP6TABLE_OWNER_MODULE</b> structure contains an array of <b>MIB_UDP6ROW_OWNER_MODULE</b> structures.

The <b>ucLocalAddr</b> member is stored in  a character array in network byte order. On Windows Vista and later, the <a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa">RtlIpv6AddressToString</a> or <a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw">RtlIpv6AddressToStringEx</a> functions may be used to convert the IPv6 address in the <b>ucLocalAddr</b> member to a string without loading the Windows Sockets DLL. 

The <b>dwLocalScopeId</b> member is in network byte order. In order to use the <b>dwLocalScopeId</b> member, the <a href="/windows/desktop/api/winsock/nf-winsock-ntohl">ntohl</a> or <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a> functions in Windows Sockets or similar functions may be needed. 

The <b>dwLocalPort</b> member are in network byte order. In order to use the <b>dwLocalPort</b> member, the <a href="/windows/desktop/api/winsock/nf-winsock-ntohs">ntohs</a> or <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a> functions in Windows Sockets or similar functions may be needed. 

The <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6table_owner_module">MIB_UDP6TABLE_OWNER_MODULE</a> structure contains the UDP listener table for IPv6 on the local computer. The name is based on the definition of this table in RFC 2454 published by the IETF. For more information, see 
<a href="http://tools.ietf.org/html/rfc2454">http://www.ietf.org/rfc/rfc2454.txt</a>. This table contains UDP  endpoints for IPv6 that have been bound to an address. It should be noted that an application can create a UDP socket and bind it to an address for the sole purpose of sending a UDP datagram, with no intention of receiving packets using this socket (functioning as a listener). 

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed. This  structure is defined in the <i>Udpmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Udpmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Udpmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedudptable">GetExtendedUdpTable</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6table_owner_module">MIB_UDP6TABLE_OWNER_MODULE</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa">RtlIpv6AddressToString</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw">RtlIpv6AddressToStringEx</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>



<a href="/windows/desktop/api/iprtrmib/ne-iprtrmib-udp_table_class">UDP_TABLE_CLASS</a>



<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a>



<a href="/windows/desktop/api/winsock/nf-winsock-ntohl">ntohl</a>



<a href="/windows/desktop/api/winsock/nf-winsock-ntohs">ntohs</a>
