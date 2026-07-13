---
UID: NS:udpmib._MIB_UDPSTATS2
title: MIB_UDPSTATS2 (udpmib.h)
description: Contains statistics for the User Datagram Protocol (UDP) running on the local computer. (MIB_UDPSTATS2)
helpviewer_keywords: ["*PMIB_UDPSTATS2","MIB_UDPSTATS2","MIB_UDPSTATS2 structure [MIB]","PMIB_UDPSTATS2","PMIB_UDPSTATS2 structure pointer [MIB]","mib.mib_udpstats2","udpmib/MIB_UDPSTATS","udpmib/PMIB_UDPSTATS2"]
old-location: mib\mib_udpstats2.htm
tech.root: MIB
ms.assetid: A225E0E7-54FB-4655-9A45-F3EF6DA1FF4E
ms.date: 12/05/2018
ms.keywords: '*PMIB_UDPSTATS2, MIB_UDPSTATS2, MIB_UDPSTATS2 structure [MIB], PMIB_UDPSTATS2, PMIB_UDPSTATS2 structure pointer [MIB], mib.mib_udpstats2, udpmib/MIB_UDPSTATS, udpmib/PMIB_UDPSTATS2'
req.header: udpmib.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: MIB_UDPSTATS2, *PMIB_UDPSTATS2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_UDPSTATS2
 - udpmib/_MIB_UDPSTATS2
 - PMIB_UDPSTATS2
 - udpmib/PMIB_UDPSTATS2
 - MIB_UDPSTATS2
 - udpmib/MIB_UDPSTATS2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - udpmib.h
api_name:
 - MIB_UDPSTATS2
---

# MIB_UDPSTATS2 structure


## -description



The 
<b>MIB_UDPSTATS2</b> structure contains statistics for the User Datagram Protocol (UDP) running on the local computer. This structure is different from <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udpstats">MIB_UDPSTATS</a> structure in that it uses 64-bit counters, rather than 32-bit counters.

## -struct-fields

### -field dw64InDatagrams

The number of datagrams received.

### -field dwNoPorts

The number of datagrams received that were discarded because the port specified was invalid.

### -field dwInErrors

The number of erroneous datagrams  received. This number does not include the value contained by the <b>dwNoPorts</b> member.

### -field dw64OutDatagrams

The number of datagrams transmitted.

### -field dwNumAddrs

The number of entries in the UDP listener table.

## -remarks

The 
			<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudpstatisticsex2">GetUdpStatisticsEx2</a> function returns a pointer to a <b>MIB_UDPSTATS2</b> structure.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcpstatisticsex2">GetTcpStatisticsEx2</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudpstatisticsex2">GetUdpStatisticsEx2</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udprow">MIB_UDPROW</a>
