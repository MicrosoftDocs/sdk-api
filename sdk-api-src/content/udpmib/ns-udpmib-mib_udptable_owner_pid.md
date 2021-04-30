---
UID: NS:udpmib._MIB_UDPTABLE_OWNER_PID
title: MIB_UDPTABLE_OWNER_PID (udpmib.h)
description: Contains the User Datagram Protocol (UDP) listener table for IPv4 on the local computer. The table also includes the process ID (PID) that issued the call to the bind function for each UDP endpoint.
helpviewer_keywords: ["*PMIB_UDPTABLE_OWNER_PID","MIB_UDPTABLE_OWNER_PID","MIB_UDPTABLE_OWNER_PID structure [MIB]","PMIB_UDPTABLE_OWNER_PID","PMIB_UDPTABLE_OWNER_PID structure pointer [MIB]","iprtrmib/MIB_UDPTABLE_OWNER_PID","iprtrmib/PMIB_UDPTABLE_OWNER_PID","mib.mib_udptable_owner_pid","udpmib/MIB_UDPTABLE_OWNER_PID","udpmib/PMIB_UDPTABLE_OWNER_PID"]
old-location: mib\mib_udptable_owner_pid.htm
tech.root: MIB
ms.assetid: 7c51a1e4-1e07-4fb1-8db3-e48229f12aca
ms.date: 12/05/2018
ms.keywords: '*PMIB_UDPTABLE_OWNER_PID, MIB_UDPTABLE_OWNER_PID, MIB_UDPTABLE_OWNER_PID structure [MIB], PMIB_UDPTABLE_OWNER_PID, PMIB_UDPTABLE_OWNER_PID structure pointer [MIB], iprtrmib/MIB_UDPTABLE_OWNER_PID, iprtrmib/PMIB_UDPTABLE_OWNER_PID, mib.mib_udptable_owner_pid, udpmib/MIB_UDPTABLE_OWNER_PID, udpmib/PMIB_UDPTABLE_OWNER_PID'
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
req.typenames: MIB_UDPTABLE_OWNER_PID, *PMIB_UDPTABLE_OWNER_PID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_UDPTABLE_OWNER_PID
 - udpmib/_MIB_UDPTABLE_OWNER_PID
 - PMIB_UDPTABLE_OWNER_PID
 - udpmib/PMIB_UDPTABLE_OWNER_PID
 - MIB_UDPTABLE_OWNER_PID
 - udpmib/MIB_UDPTABLE_OWNER_PID
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
 - MIB_UDPTABLE_OWNER_PID
---

# MIB_UDPTABLE_OWNER_PID structure


## -description

The <b>MIB_UDPTABLE_OWNER_PID</b> structure contains the User Datagram Protocol (UDP)  listener table for IPv4 on the local computer. The table also includes the process ID (PID) that issued the call to the <a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function for each UDP endpoint.

## -struct-fields

### -field dwNumEntries

The number of <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udprow_owner_pid">MIB_UDPROW_OWNER_PID</a> elements in <b>table</b>.

### -field table

An array of <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udprow_owner_pid">MIB_UDPROW_OWNER_PID</a> structures returned by a call to <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedudptable">GetExtendedUdpTable</a>.

## -remarks

The <b>MIB_UDPTABLE_OWNER_PID</b> structure is returned by a call to <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedudptable">GetExtendedUdpTable</a> with the <i>TableClass</i> parameter set to <b>UDP_TABLE_OWNER_PID</b> from the <a href="/windows/desktop/api/iprtrmib/ne-iprtrmib-udp_table_class">UDP_TABLE_CLASS</a> enumeration and the <i>ulAf</i> parameter set to <b>AF_INET4</b>. The <b>MIB_UDPTABLE_OWNER_PID</b> structure contains an array of <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udprow_owner_pid">MIB_UDPROW_OWNER_PID</a> structures.

The <b>MIB_UDPTABLE_OWNER_PID</b> structure may contain padding for alignment between the <b>dwNumEntries</b> member and the first <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udprow_owner_pid">MIB_UDPROW_OWNER_PID</a> array entry in the <b>table</b> member. Padding for alignment may also be present between the <b>MIB_UDPROW_OWNER_PID</b> array entries in the <b>table</b> member. Any access to a <b>MIB_UDPROW_OWNER_PID</b> array entry should assume  padding may exist. 



The <b>MIB_UDPTABLE_OWNER_PID</b> structure contains the UDP listener table for IPv4 on the local computer. The name is based on the definition of this table in RFC 1213 published by the IETF. For more information, see 
<a href="http://tools.ietf.org/html/rfc1213">http://www.ietf.org/rfc/rfc1213.txt</a>. This table contains UDP  endpoints for IPv4 that have been bound to an address. It should be noted that an application can create a UDP socket and bind it to an address for the sole purpose of sending a UDP datagram, with no intention of receiving packets using this socket (functioning as a listener). 

The <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable_owner_module">MIB_UDPTABLE_OWNER_MODULE</a> structure is an enhanced version of the  <b>MIB_UDPTABLE_OWNER_PID</b> structure that includes any available ownership data for each UDP endpoint in the table.  The <b>MIB_UDPTABLE_OWNER_PID</b> is an enhanced version of the <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable">MIB_UDPTABLE</a> that includes the process ID (PID) that issued the call to the <a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function for each UDP endpoint in the table.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vistaand later, the organization of header files has changed. This  structure is defined in the <i>Udpmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Udpmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Udpmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedudptable">GetExtendedUdpTable</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudp6table">GetUdp6Table</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudptable">GetUdpTable</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6row">MIB_UDP6ROW</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6row_owner_module">MIB_UDP6ROW_OWNER_MODULE</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6row_owner_pid">MIB_UDP6ROW_OWNER_PID</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6table">MIB_UDP6TABLE</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6table_owner_module">MIB_UDP6TABLE_OWNER_MODULE</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6table_owner_pid">MIB_UDP6TABLE_OWNER_PID</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udprow">MIB_UDPROW</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udprow_owner_module">MIB_UDPROW_OWNER_MODULE</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udprow_owner_pid">MIB_UDPROW_OWNER_PID</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable">MIB_UDPTABLE</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable_owner_module">MIB_UDPTABLE_OWNER_MODULE</a>



<a href="/windows/desktop/api/iprtrmib/ne-iprtrmib-udp_table_class">UDP_TABLE_CLASS</a>



<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>