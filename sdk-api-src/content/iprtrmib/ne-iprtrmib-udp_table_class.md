---
UID: NE:iprtrmib._UDP_TABLE_CLASS
title: UDP_TABLE_CLASS (iprtrmib.h)
description: Defines the set of values used to indicate the type of table returned by calls to GetExtendedUdpTable.
helpviewer_keywords: ["*PUDP_TABLE_CLASS","PUDP_TABLE_CLASS","PUDP_TABLE_CLASS enumeration pointer [IP Helper]","UDP_TABLE_BASIC","UDP_TABLE_CLASS","UDP_TABLE_CLASS enumeration [IP Helper]","UDP_TABLE_OWNER_MODULE","UDP_TABLE_OWNER_PID","iphlp.udp_table_class","iphlpapi/PUDP_TABLE_CLASS","iphlpapi/UDP_TABLE_BASIC","iphlpapi/UDP_TABLE_CLASS","iphlpapi/UDP_TABLE_OWNER_MODULE","iphlpapi/UDP_TABLE_OWNER_PID","iprtrmib/PUDP_TABLE_CLASS","iprtrmib/UDP_TABLE_BASIC","iprtrmib/UDP_TABLE_CLASS","iprtrmib/UDP_TABLE_OWNER_MODULE","iprtrmib/UDP_TABLE_OWNER_PID"]
old-location: iphlp\udp_table_class.htm
tech.root: IpHlp
ms.assetid: 2e7304d1-b89c-46d4-9121-936a1c38cc51
ms.date: 12/05/2018
ms.keywords: '*PUDP_TABLE_CLASS, PUDP_TABLE_CLASS, PUDP_TABLE_CLASS enumeration pointer [IP Helper], UDP_TABLE_BASIC, UDP_TABLE_CLASS, UDP_TABLE_CLASS enumeration [IP Helper], UDP_TABLE_OWNER_MODULE, UDP_TABLE_OWNER_PID, iphlp.udp_table_class, iphlpapi/PUDP_TABLE_CLASS, iphlpapi/UDP_TABLE_BASIC, iphlpapi/UDP_TABLE_CLASS, iphlpapi/UDP_TABLE_OWNER_MODULE, iphlpapi/UDP_TABLE_OWNER_PID, iprtrmib/PUDP_TABLE_CLASS, iprtrmib/UDP_TABLE_BASIC, iprtrmib/UDP_TABLE_CLASS, iprtrmib/UDP_TABLE_OWNER_MODULE, iprtrmib/UDP_TABLE_OWNER_PID'
req.header: iprtrmib.h
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
req.typenames: UDP_TABLE_CLASS, *PUDP_TABLE_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _UDP_TABLE_CLASS
 - iprtrmib/_UDP_TABLE_CLASS
 - PUDP_TABLE_CLASS
 - iprtrmib/PUDP_TABLE_CLASS
 - UDP_TABLE_CLASS
 - iprtrmib/UDP_TABLE_CLASS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iprtrmib.h
 - Iphlpapi.h
api_name:
 - UDP_TABLE_CLASS
---

# UDP_TABLE_CLASS enumeration


## -description

The <b>UDP_TABLE_CLASS</b> enumeration defines the set of values used to  indicate the type of table returned by calls to <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedudptable">GetExtendedUdpTable</a>.

## -enum-fields

### -field UDP_TABLE_BASIC

A <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable">MIB_UDPTABLE</a> structure that contains all UDP endpoints on the local computer is returned to the caller.

### -field UDP_TABLE_OWNER_PID

A <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable_owner_pid">MIB_UDPTABLE_OWNER_PID</a> or <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6table_owner_pid">MIB_UDP6TABLE_OWNER_PID</a> structure that contains all UDP endpoints on the local computer is returned to the caller.

### -field UDP_TABLE_OWNER_MODULE

A <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable_owner_module">MIB_UDPTABLE_OWNER_MODULE</a> or <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6table_owner_module">MIB_UDP6TABLE_OWNER_MODULE</a> structure that contains all  UDP endpoints on the local computer is returned to the caller.

## -remarks

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>UDP_TABLE_CLASS</b> enumeration  is defined in the <i>Iprtrmib.h</i> header file, not in the <i>Iphlpapi.h</i> header file. Note that the <i>Iprtrmib.h</i> header file is automatically included in <i>Iphlpapi.h</i> header file. The <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedudptable">GetExtendedUdpTable</a>