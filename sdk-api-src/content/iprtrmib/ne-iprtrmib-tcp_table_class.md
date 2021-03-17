---
UID: NE:iprtrmib._TCP_TABLE_CLASS
title: TCP_TABLE_CLASS (iprtrmib.h)
description: Defines the set of values used to indicate the type of table returned by calls to GetExtendedTcpTable.
helpviewer_keywords: ["*PTCP_TABLE_CLASS","PTCP_TABLE_CLASS","PTCP_TABLE_CLASS enumeration pointer [IP Helper]","TCP_TABLE_BASIC_ALL","TCP_TABLE_BASIC_CONNECTIONS","TCP_TABLE_BASIC_LISTENER","TCP_TABLE_CLASS","TCP_TABLE_CLASS enumeration [IP Helper]","TCP_TABLE_OWNER_MODULE_ALL","TCP_TABLE_OWNER_MODULE_CONNECTIONS","TCP_TABLE_OWNER_MODULE_LISTENER","TCP_TABLE_OWNER_PID_ALL","TCP_TABLE_OWNER_PID_CONNECTIONS","TCP_TABLE_OWNER_PID_LISTENER","iphlp.tcp_table_class","iphlpapi/PTCP_TABLE_CLASS","iphlpapi/TCP_TABLE_BASIC_ALL","iphlpapi/TCP_TABLE_BASIC_CONNECTIONS","iphlpapi/TCP_TABLE_BASIC_LISTENER","iphlpapi/TCP_TABLE_CLASS","iphlpapi/TCP_TABLE_OWNER_MODULE_ALL","iphlpapi/TCP_TABLE_OWNER_MODULE_CONNECTIONS","iphlpapi/TCP_TABLE_OWNER_MODULE_LISTENER","iphlpapi/TCP_TABLE_OWNER_PID_ALL","iphlpapi/TCP_TABLE_OWNER_PID_CONNECTIONS","iphlpapi/TCP_TABLE_OWNER_PID_LISTENER","iprtrmib/PTCP_TABLE_CLASS","iprtrmib/TCP_TABLE_BASIC_ALL","iprtrmib/TCP_TABLE_BASIC_CONNECTIONS","iprtrmib/TCP_TABLE_BASIC_LISTENER","iprtrmib/TCP_TABLE_CLASS","iprtrmib/TCP_TABLE_OWNER_MODULE_ALL","iprtrmib/TCP_TABLE_OWNER_MODULE_CONNECTIONS","iprtrmib/TCP_TABLE_OWNER_MODULE_LISTENER","iprtrmib/TCP_TABLE_OWNER_PID_ALL","iprtrmib/TCP_TABLE_OWNER_PID_CONNECTIONS","iprtrmib/TCP_TABLE_OWNER_PID_LISTENER"]
old-location: iphlp\tcp_table_class.htm
tech.root: IpHlp
ms.assetid: abfaf7e5-7739-4f23-bfb4-09206111599f
ms.date: 12/05/2018
ms.keywords: '*PTCP_TABLE_CLASS, PTCP_TABLE_CLASS, PTCP_TABLE_CLASS enumeration pointer [IP Helper], TCP_TABLE_BASIC_ALL, TCP_TABLE_BASIC_CONNECTIONS, TCP_TABLE_BASIC_LISTENER, TCP_TABLE_CLASS, TCP_TABLE_CLASS enumeration [IP Helper], TCP_TABLE_OWNER_MODULE_ALL, TCP_TABLE_OWNER_MODULE_CONNECTIONS, TCP_TABLE_OWNER_MODULE_LISTENER, TCP_TABLE_OWNER_PID_ALL, TCP_TABLE_OWNER_PID_CONNECTIONS, TCP_TABLE_OWNER_PID_LISTENER, iphlp.tcp_table_class, iphlpapi/PTCP_TABLE_CLASS, iphlpapi/TCP_TABLE_BASIC_ALL, iphlpapi/TCP_TABLE_BASIC_CONNECTIONS, iphlpapi/TCP_TABLE_BASIC_LISTENER, iphlpapi/TCP_TABLE_CLASS, iphlpapi/TCP_TABLE_OWNER_MODULE_ALL, iphlpapi/TCP_TABLE_OWNER_MODULE_CONNECTIONS, iphlpapi/TCP_TABLE_OWNER_MODULE_LISTENER, iphlpapi/TCP_TABLE_OWNER_PID_ALL, iphlpapi/TCP_TABLE_OWNER_PID_CONNECTIONS, iphlpapi/TCP_TABLE_OWNER_PID_LISTENER, iprtrmib/PTCP_TABLE_CLASS, iprtrmib/TCP_TABLE_BASIC_ALL, iprtrmib/TCP_TABLE_BASIC_CONNECTIONS, iprtrmib/TCP_TABLE_BASIC_LISTENER, iprtrmib/TCP_TABLE_CLASS, iprtrmib/TCP_TABLE_OWNER_MODULE_ALL, iprtrmib/TCP_TABLE_OWNER_MODULE_CONNECTIONS, iprtrmib/TCP_TABLE_OWNER_MODULE_LISTENER, iprtrmib/TCP_TABLE_OWNER_PID_ALL, iprtrmib/TCP_TABLE_OWNER_PID_CONNECTIONS, iprtrmib/TCP_TABLE_OWNER_PID_LISTENER'
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
req.typenames: TCP_TABLE_CLASS, *PTCP_TABLE_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TCP_TABLE_CLASS
 - iprtrmib/_TCP_TABLE_CLASS
 - PTCP_TABLE_CLASS
 - iprtrmib/PTCP_TABLE_CLASS
 - TCP_TABLE_CLASS
 - iprtrmib/TCP_TABLE_CLASS
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
 - TCP_TABLE_CLASS
---

# TCP_TABLE_CLASS enumeration


## -description

The <b>TCP_TABLE_CLASS</b> enumeration defines the set of values used to  indicate the type of table returned by  calls to <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedtcptable">GetExtendedTcpTable</a>.

## -enum-fields

### -field TCP_TABLE_BASIC_LISTENER

A <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable">MIB_TCPTABLE</a> table that contains all listening (receiving only) TCP endpoints on the local computer is returned to the caller.

### -field TCP_TABLE_BASIC_CONNECTIONS

A <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable">MIB_TCPTABLE</a> table that contains all connected TCP endpoints  on the local computer is returned to the caller.

### -field TCP_TABLE_BASIC_ALL

A <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable">MIB_TCPTABLE</a> table that contains all TCP endpoints  on the local computer is returned to the caller.

### -field TCP_TABLE_OWNER_PID_LISTENER

A <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable_owner_pid">MIB_TCPTABLE_OWNER_PID</a> or <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table_owner_pid">MIB_TCP6TABLE_OWNER_PID</a> that contains all listening (receiving only) TCP endpoints on the local computer is returned to the caller.

### -field TCP_TABLE_OWNER_PID_CONNECTIONS

A <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable_owner_pid">MIB_TCPTABLE_OWNER_PID</a> or <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table_owner_pid">MIB_TCP6TABLE_OWNER_PID</a> that structure that contains all connected TCP endpoints  on the local computer is returned to the caller.

### -field TCP_TABLE_OWNER_PID_ALL

A <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable_owner_pid">MIB_TCPTABLE_OWNER_PID</a> or <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table_owner_pid">MIB_TCP6TABLE_OWNER_PID</a> structure that contains all TCP endpoints  on the local computer is returned to the caller.

### -field TCP_TABLE_OWNER_MODULE_LISTENER

A <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable_owner_module">MIB_TCPTABLE_OWNER_MODULE</a> or <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table_owner_module">MIB_TCP6TABLE_OWNER_MODULE</a> structure that contains all listening (receiving only) TCP endpoints on the local computer is returned to the caller.

### -field TCP_TABLE_OWNER_MODULE_CONNECTIONS

A <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable_owner_module">MIB_TCPTABLE_OWNER_MODULE</a> or <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table_owner_module">MIB_TCP6TABLE_OWNER_MODULE</a> structure that contains all connected TCP endpoints on the local computer is returned to the caller.

### -field TCP_TABLE_OWNER_MODULE_ALL

A <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable_owner_module">MIB_TCPTABLE_OWNER_MODULE</a> or <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table_owner_module">MIB_TCP6TABLE_OWNER_MODULE</a> structure that contains all  TCP endpoints on the local computer is returned to the caller.

## -remarks

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>TCP_TABLE_CLASS</b> enumeration  is defined in the <i>Iprtrmib.h</i> header file, not in the <i>Iphlpapi.h</i> header file. Note that the <i>Iprtrmib.h</i> header file is automatically included in <i>Iphlpapi.h</i> header file. The <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedtcptable">GetExtendedTcpTable</a>