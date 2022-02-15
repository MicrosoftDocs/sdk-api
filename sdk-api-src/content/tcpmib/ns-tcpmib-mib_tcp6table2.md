---
UID: NS:tcpmib._MIB_TCP6TABLE2
title: MIB_TCP6TABLE2 (tcpmib.h)
description: Contains a table of IPv6 TCP connections on the local computer.
helpviewer_keywords: ["*PMIB_TCP6TABLE2","MIB_TCP6TABLE2","MIB_TCP6TABLE2 structure [MIB]","PMIB_TCP6TABLE2","PMIB_TCP6TABLE2 structure pointer [MIB]","mib.mib_tcp6table2","tcpmib/MIB_TCP6TABLE2","tcpmib/PMIB_TCP6TABLE2"]
old-location: mib\mib_tcp6table2.htm
tech.root: MIB
ms.assetid: 3cb8568e-ce31-4ed1-aa9e-abcb826c0cea
ms.date: 12/05/2018
ms.keywords: '*PMIB_TCP6TABLE2, MIB_TCP6TABLE2, MIB_TCP6TABLE2 structure [MIB], PMIB_TCP6TABLE2, PMIB_TCP6TABLE2 structure pointer [MIB], mib.mib_tcp6table2, tcpmib/MIB_TCP6TABLE2, tcpmib/PMIB_TCP6TABLE2'
req.header: tcpmib.h
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
req.typenames: MIB_TCP6TABLE2, *PMIB_TCP6TABLE2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_TCP6TABLE2
 - tcpmib/_MIB_TCP6TABLE2
 - PMIB_TCP6TABLE2
 - tcpmib/PMIB_TCP6TABLE2
 - MIB_TCP6TABLE2
 - tcpmib/MIB_TCP6TABLE2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tcpmib.h
api_name:
 - MIB_TCP6TABLE2
---

# MIB_TCP6TABLE2 structure


## -description

The 
<b>MIB_TCP6TABLE2</b> structure contains a table of IPv6 TCP connections on the local computer.

## -struct-fields

### -field dwNumEntries

A value that specifies the number of TCP connections in the array.

### -field table

An array of 
<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row2">MIB_TCP6ROW2</a> structures containing TCP connection entries.

## -remarks

The <b>MIB_TCP6TABLE2</b> structure is defined on Windows Vista and later. 

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcp6table2">GetTcp6Table2</a> function retrieves the IPv6 TCP connection table on the local computer and returns this information in a <b>MIB_TCP6TABLE2</b> structure. 

An array of <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row2">MIB_TCP6ROW2</a> structures are contained in the <b>MIB_TCP6TABLE2</b> structure. 

The <b>MIB_TCP6TABLE2</b> structure may contain padding for alignment between the <b>dwNumEntries</b> member and the first <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row2">MIB_TCP6ROW2</a> array entry in the <b>table</b> member. Padding for alignment may also be present between the <b>MIB_TCP6ROW2</b> array entries in the <b>table</b> member. Any access to a <b>MIB_TCP6ROW2</b> array entry should assume  padding may exist.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcp6table">GetTcp6Table</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcp6table2">GetTcp6Table2</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcptable">GetTcpTable</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcptable2">GetTcpTable2</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row">MIB_TCP6ROW</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row2">MIB_TCP6ROW2</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table">MIB_TCP6TABLE</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcprow_lh">MIB_TCPROW</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcprow2">MIB_TCPROW2</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable">MIB_TCPTABLE</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable2">MIB_TCPTABLE2</a>