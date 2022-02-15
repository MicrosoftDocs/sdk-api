---
UID: NS:tcpmib._MIB_TCP6TABLE_OWNER_MODULE
title: MIB_TCP6TABLE_OWNER_MODULE (tcpmib.h)
description: Contains a table of process IDs (PIDs) and the IPv6 TCP links context bound to these PIDs with any available ownership data.
helpviewer_keywords: ["*PMIB_TCP6TABLE_OWNER_MODULE","MIB_TCP6TABLE_OWNER_MODULE","MIB_TCP6TABLE_OWNER_MODULE structure [MIB]","PMIB_TCP6TABLE_OWNER_MODULE","PMIB_TCP6TABLE_OWNER_MODULE structure pointer [MIB]","iprtrmib/MIB_TCP6TABLE_OWNER_MODULE","iprtrmib/PMIB_TCP6TABLE_OWNER_MODULE","mib.mib_tcp6table_owner_module","tcpmib/MIB_TCP6TABLE_OWNER_MODULE","tcpmib/PMIB_TCP6TABLE_OWNER_MODULE"]
old-location: mib\mib_tcp6table_owner_module.htm
tech.root: MIB
ms.assetid: aa52531c-1d4e-44f9-8638-1528beb491f3
ms.date: 12/05/2018
ms.keywords: '*PMIB_TCP6TABLE_OWNER_MODULE, MIB_TCP6TABLE_OWNER_MODULE, MIB_TCP6TABLE_OWNER_MODULE structure [MIB], PMIB_TCP6TABLE_OWNER_MODULE, PMIB_TCP6TABLE_OWNER_MODULE structure pointer [MIB], iprtrmib/MIB_TCP6TABLE_OWNER_MODULE, iprtrmib/PMIB_TCP6TABLE_OWNER_MODULE, mib.mib_tcp6table_owner_module, tcpmib/MIB_TCP6TABLE_OWNER_MODULE, tcpmib/PMIB_TCP6TABLE_OWNER_MODULE'
req.header: tcpmib.h
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
req.typenames: MIB_TCP6TABLE_OWNER_MODULE, *PMIB_TCP6TABLE_OWNER_MODULE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_TCP6TABLE_OWNER_MODULE
 - tcpmib/_MIB_TCP6TABLE_OWNER_MODULE
 - PMIB_TCP6TABLE_OWNER_MODULE
 - tcpmib/PMIB_TCP6TABLE_OWNER_MODULE
 - MIB_TCP6TABLE_OWNER_MODULE
 - tcpmib/MIB_TCP6TABLE_OWNER_MODULE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tcpmib.h
 - Iprtrmib.h
api_name:
 - MIB_TCP6TABLE_OWNER_MODULE
---

# MIB_TCP6TABLE_OWNER_MODULE structure


## -description

The <b>MIB_TCP6TABLE_OWNER_MODULE</b> structure contains a table of process IDs (PIDs) and the IPv6 TCP links context bound to these PIDs with any available ownership data.

## -struct-fields

### -field dwNumEntries

The number of <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row_owner_module">MIB_TCP6ROW_OWNER_MODULE</a> elements in the <b>table</b>.

### -field table

Array of <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row_owner_module">MIB_TCP6ROW_OWNER_MODULE</a> structures returned by a call to <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedtcptable">GetExtendedTcpTable</a>.

## -remarks

The <b>MIB_TCP6TABLE_OWNER_MODULE</b> structure is returned by a call to <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedtcptable">GetExtendedTcpTable</a> with the <i>TableClass</i> parameter set to a  <b>TCP_TABLE_OWNER_MODULE_LISTENER</b>, <b>TCP_TABLE_OWNER_MODULE_CONNECTIONS</b>, or <b>TCP_TABLE_OWNER_MODULE_ALL</b> from the <a href="/windows/desktop/api/iprtrmib/ne-iprtrmib-tcp_table_class">TCP_TABLE_CLASS</a> enumeration and the <i>ulAf</i> parameter set to <b>AF_INET6</b>.

The <b>MIB_TCP6TABLE_OWNER_MODULE</b> structure may contain padding for alignment between the <b>dwNumEntries</b> member and the first <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row_owner_module">MIB_TCP6ROW_OWNER_MODULE</a> array entry in the <b>table</b> member. Padding for alignment may also be present between the <b>MIB_TCP6ROW_OWNER_MODULE</b> array entries in the <b>table</b> member. Any access to a <b>MIB_TCP6ROW_OWNER_MODULE</b> array entry should assume  padding may exist. 



On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed. This  structure is defined in the <i>Tcpmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Tcpmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Tcpmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/previous-versions/windows/desktop/mib/management-information-base-reference">MIB Reference</a>



<a href="/previous-versions/windows/desktop/mib/mib-structures">MIB Structures</a>