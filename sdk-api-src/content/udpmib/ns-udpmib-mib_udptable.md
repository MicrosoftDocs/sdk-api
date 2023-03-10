---
UID: NS:udpmib._MIB_UDPTABLE
title: MIB_UDPTABLE (udpmib.h)
description: Contains the User Datagram Protocol (UDP) listener table for IPv4 on the local computer.
helpviewer_keywords: ["*PMIB_UDPTABLE","MIB_UDPTABLE","MIB_UDPTABLE structure [MIB]","PMIB_UDPTABLE","PMIB_UDPTABLE structure pointer [MIB]","_mpr_mib_udptable","iprtrmib/MIB_UDPTABLE","iprtrmib/PMIB_UDPTABLE","mib.mib_udptable","rras.mib_udptable","udpmib/MIB_UDPTABLE","udpmib/PMIB_UDPTABLE"]
old-location: mib\mib_udptable.htm
tech.root: MIB
ms.assetid: 83608d38-e352-483a-b284-2f9cb444e64f
ms.date: 12/05/2018
ms.keywords: '*PMIB_UDPTABLE, MIB_UDPTABLE, MIB_UDPTABLE structure [MIB], PMIB_UDPTABLE, PMIB_UDPTABLE structure pointer [MIB], _mpr_mib_udptable, iprtrmib/MIB_UDPTABLE, iprtrmib/PMIB_UDPTABLE, mib.mib_udptable, rras.mib_udptable, udpmib/MIB_UDPTABLE, udpmib/PMIB_UDPTABLE'
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
req.typenames: MIB_UDPTABLE, *PMIB_UDPTABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_UDPTABLE
 - udpmib/_MIB_UDPTABLE
 - PMIB_UDPTABLE
 - udpmib/PMIB_UDPTABLE
 - MIB_UDPTABLE
 - udpmib/MIB_UDPTABLE
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
 - MIB_UDPTABLE
---

# MIB_UDPTABLE structure


## -description

The 
<b>MIB_UDPTABLE</b> structure contains the User Datagram Protocol (UDP)  listener table for IPv4 on the local computer.

## -struct-fields

### -field dwNumEntries

The number of entries in the table.

### -field table

A pointer to an array of 
<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udprow">MIB_UDPROW</a> structures.

## -remarks

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudptable">GetUdpTable</a> function enumerates the table of UDP  endpoints for IPv4 that have been bound to an address on the local computer and returns this information in a <b>MIB_UDPTABLE</b> structure. 

This table includes the local IPv4 address and port information for sending and receiving UDP datagrams on the local computer. An array of <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udprow">MIB_UDPROW</a> structures are contained in the <b>MIB_UDPTABLE</b> structure.

The <b>MIB_UDPTABLE</b> structure may contain padding for alignment between the <b>dwNumEntries</b> member and the first <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udprow">MIB_UDPROW</a> array entry in the <b>table</b> member. Padding for alignment may also be present between the <b>MIB_UDPROW</b> array entries in the <b>table</b> member. Any access to a <b>MIB_UDPROW</b> array entry should assume  padding may exist. 



The <b>MIB_UDPTABLE</b> structure contains the UDP listener table for IPv4 on the local computer. The name is based on the definition of this table in RFC 1213 published by the IETF. For more information, see 
<a href="http://tools.ietf.org/html/rfc1213">http://www.ietf.org/rfc/rfc1213.txt</a>. This table contains UDP  endpoints for IPv4 that have been bound to an address. It should be noted that an application can create a UDP socket and bind it to an address for the sole purpose of sending a UDP datagram, with no intention of receiving packets using this socket (functioning as a listener). 

The <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable_owner_module">MIB_UDPTABLE_OWNER_MODULE</a> structure is an enhanced version of the  <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable_owner_pid">MIB_UDPTABLE_OWNER_PID</a> structure that includes any available ownership data for each UDP endpoint in the table.  The <b>MIB_UDPTABLE_OWNER_PID</b> is an enhanced version of the <b>MIB_UDPTABLE</b> that includes the process ID (PID) that issued the call to the <a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function for each UDP endpoint in the table.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed. This  structure is defined in the <i>Udpmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Udpmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Udpmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

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



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable_owner_module">MIB_UDPTABLE_OWNER_MODULE</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable_owner_pid">MIB_UDPTABLE_OWNER_PID</a>



<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>