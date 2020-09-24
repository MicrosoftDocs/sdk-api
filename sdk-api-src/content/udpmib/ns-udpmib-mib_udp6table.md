---
UID: NS:udpmib._MIB_UDP6TABLE
title: MIB_UDP6TABLE (udpmib.h)
description: Contains the User Datagram Protocol (UDP) listener table for IPv6 on the local computer.
helpviewer_keywords: ["*PMIB_UDP6TABLE","MIB_UDP6TABLE","MIB_UDP6TABLE structure [MIB]","PMIB_UDP6TABLE","PMIB_UDP6TABLE structure pointer [MIB]","mib.mib_udp6table","udpmib/MIB_UDP6TABLE","udpmib/PMIB_UDP6TABLE"]
old-location: mib\mib_udp6table.htm
tech.root: MIB
ms.assetid: 49da9a1f-f244-464e-96b2-944a286445d4
ms.date: 12/05/2018
ms.keywords: '*PMIB_UDP6TABLE, MIB_UDP6TABLE, MIB_UDP6TABLE structure [MIB], PMIB_UDP6TABLE, PMIB_UDP6TABLE structure pointer [MIB], mib.mib_udp6table, udpmib/MIB_UDP6TABLE, udpmib/PMIB_UDP6TABLE'
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
req.typenames: MIB_UDP6TABLE, *PMIB_UDP6TABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_UDP6TABLE
 - udpmib/_MIB_UDP6TABLE
 - PMIB_UDP6TABLE
 - udpmib/PMIB_UDP6TABLE
 - MIB_UDP6TABLE
 - udpmib/MIB_UDP6TABLE
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
 - MIB_UDP6TABLE
---

# MIB_UDP6TABLE structure


## -description

The 
<b>MIB_UDP6TABLE</b> structure contains the User Datagram Protocol (UDP)  listener table for IPv6 on the local computer.

## -struct-fields

### -field dwNumEntries

The number of entries in the table.

### -field table

A pointer to an array of 
<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6row">MIB_UDP6ROW</a> structures.

## -remarks

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudp6table">GetUdp6Table</a> function enumerates the UDP  endpoints for IPv6 that have been bound to an address on the local computer and returns this information in a <b>MIB_UDP6TABLE</b> structure. 

This table includes the local IPv6 address, scope ID, and port information for sending and receiving UDP datagrams on the local computer. An array of <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6row">MIB_UDP6ROW</a> structures are contained in the <b>MIB_UDP6TABLE</b> structure.

The <b>MIB_UDP6TABLE</b> structure may contain padding for alignment between the <b>dwNumEntries</b> member and the first <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6row">MIB_UDP6ROW</a> array entry in the <b>table</b> member. Padding for alignment may also be present between the <b>MIB_UDP6ROW</b> array entries in the <b>table</b> member. Any access to a <b>MIB_UDP6ROW</b> array entry should assume  padding may exist. 



The <b>MIB_UDP6TABLE</b> structure contains the UDP listener table for IPv6 on the local computer. The name is based on the definition of this table in RFC 2454 published by the IETF. For more information, see 
<a href="http://tools.ietf.org/html/rfc2454">http://www.ietf.org/rfc/rfc2454.txt</a>. This table contains UDP  endpoints for IPv6 that have been bound to an address. It should be noted that an application can create a UDP socket and bind it to an address for the sole purpose of sending a UDP datagram, with no intention of receiving packets using this socket (functioning as a listener). 



The <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6table_owner_module">MIB_UDP6TABLE_OWNER_MODULE</a> structure is an enhanced version of the  <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6table_owner_pid">MIB_UDP6TABLE_OWNER_PID</a> structure that includes any available ownership data for each UDP endpoint in the table.  The <b>MIB_UDP6TABLE_OWNER_PID</b> is an enhanced version of the <b>MIB_UDP6TABLE</b> that includes the process ID (PID) that issued the call to the <a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function for each UDP endpoint in the table.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedudptable">GetExtendedUdpTable</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudp6table">GetUdp6Table</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudptable">GetUdpTable</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6row">MIB_UDP6ROW</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6row_owner_module">MIB_UDP6ROW_OWNER_MODULE</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6row_owner_pid">MIB_UDP6ROW_OWNER_PID</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6table_owner_module">MIB_UDP6TABLE_OWNER_MODULE</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6table_owner_pid">MIB_UDP6TABLE_OWNER_PID</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udprow">MIB_UDPROW</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udprow_owner_module">MIB_UDPROW_OWNER_MODULE</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udprow_owner_pid">MIB_UDPROW_OWNER_PID</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable">MIB_UDPTABLE</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable_owner_module">MIB_UDPTABLE_OWNER_MODULE</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable_owner_pid">MIB_UDPTABLE_OWNER_PID</a>



<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>