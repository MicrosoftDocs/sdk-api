---
UID: NS:tcpmib._MIB_TCPTABLE_OWNER_PID
title: MIB_TCPTABLE_OWNER_PID (tcpmib.h)
description: Contains a table of process IDs (PIDs) and the IPv4 TCP links that are context bound to these PIDs.
helpviewer_keywords: ["*PMIB_TCPTABLE_OWNER_PID","MIB_TCPTABLE_OWNER_PID","MIB_TCPTABLE_OWNER_PID structure [MIB]","PMIB_TCPTABLE_OWNER_PID","PMIB_TCPTABLE_OWNER_PID structure pointer [MIB]","iprtrmib/MIB_TCPTABLE_OWNER_PID","iprtrmib/PMIB_TCPTABLE_OWNER_PID","mib.mib_tcptable_owner_pid","tcpmib/MIB_TCPTABLE_OWNER_PID","tcpmib/PMIB_TCPTABLE_OWNER_PID"]
old-location: mib\mib_tcptable_owner_pid.htm
tech.root: MIB
ms.assetid: ef39b832-1f22-468a-8734-c7d9bd3ac965
ms.date: 12/05/2018
ms.keywords: '*PMIB_TCPTABLE_OWNER_PID, MIB_TCPTABLE_OWNER_PID, MIB_TCPTABLE_OWNER_PID structure [MIB], PMIB_TCPTABLE_OWNER_PID, PMIB_TCPTABLE_OWNER_PID structure pointer [MIB], iprtrmib/MIB_TCPTABLE_OWNER_PID, iprtrmib/PMIB_TCPTABLE_OWNER_PID, mib.mib_tcptable_owner_pid, tcpmib/MIB_TCPTABLE_OWNER_PID, tcpmib/PMIB_TCPTABLE_OWNER_PID'
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
req.typenames: MIB_TCPTABLE_OWNER_PID, *PMIB_TCPTABLE_OWNER_PID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_TCPTABLE_OWNER_PID
 - tcpmib/_MIB_TCPTABLE_OWNER_PID
 - PMIB_TCPTABLE_OWNER_PID
 - tcpmib/PMIB_TCPTABLE_OWNER_PID
 - MIB_TCPTABLE_OWNER_PID
 - tcpmib/MIB_TCPTABLE_OWNER_PID
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
 - MIB_TCPTABLE_OWNER_PID
---

# MIB_TCPTABLE_OWNER_PID structure


## -description

The <b>MIB_TCPTABLE_OWNER_PID</b> structure contains a table of process IDs (PIDs)  and the IPv4 TCP links that  are context bound to these PIDs.

## -struct-fields

### -field dwNumEntries

The number of <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcprow_owner_pid">MIB_TCPROW_OWNER_PID</a> elements in the <b>table</b>.

### -field table

Array of <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcprow_owner_pid">MIB_TCPROW_OWNER_PID</a> structures returned by a call to <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedtcptable">GetExtendedTcpTable</a>.

## -remarks

This table is specifically returned by a call to <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedtcptable">GetExtendedTcpTable</a> with the <i>TableClass</i> parameter set to a <b>TCP_TABLE_OWNER_PID_*</b> value from the <a href="/windows/desktop/api/iprtrmib/ne-iprtrmib-tcp_table_class">TCP_TABLE_CLASS</a> enumeration and the <i>ulAf</i> parameter set to <b>AF_INET</b>.

The <b>MIB_TCPTABLE_OWNER_PID</b> structure may contain padding for alignment between the <b>dwNumEntries</b> member and the first <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcprow_owner_pid">MIB_TCPROW_OWNER_PID</a> array entry in the <b>table</b> member. Padding for alignment may also be present between the <b>MIB_TCPROW_OWNER_PID</b> array entries in the <b>table</b> member. Any access to a <b>MIB_TCPROW_OWNER_PID</b> array entry should assume  padding may exist. 



On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed. This  structure is defined in the <i>Tcpmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Tcpmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Tcpmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/previous-versions/windows/desktop/mib/management-information-base-reference">MIB Reference</a>



<a href="/previous-versions/windows/desktop/mib/mib-structures">MIB Structures</a>