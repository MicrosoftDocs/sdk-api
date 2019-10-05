---
UID: NS:udpmib._MIB_UDPSTATS
title: MIB_UDPSTATS (udpmib.h)
author: windows-sdk-content
description: Contains statistics for the User Datagram Protocol (UDP) running on the local computer.
old-location: mib\mib_udpstats.htm
tech.root: MIB
ms.assetid: 128bae44-59a2-4e37-a588-a18805b9e340
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PMIB_UDPSTATS, MIB_UDPSTATS, MIB_UDPSTATS structure [MIB], PMIB_UDPSTATS, PMIB_UDPSTATS structure pointer [MIB], _mpr_mib_udpstats, iprtrmib/MIB_UDPSTATS, iprtrmib/PMIB_UDPSTATS, mib.mib_udpstats, rras.mib_udpstats, udpmib/MIB_UDPSTATS, udpmib/PMIB_UDPSTATS'
ms.topic: struct
f1_keywords:
- udpmib/MIB_UDPSTATS
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Udpmib.h
- Iprtrmib.h
api_name:
- MIB_UDPSTATS
targetos: Windows
req.typenames: MIB_UDPSTATS, *PMIB_UDPSTATS
req.redist: 
ms.custom: 19H1
---

# MIB_UDPSTATS structure


## -description


The 
<b>MIB_UDPSTATS</b> structure contains statistics for the User Datagram Protocol (UDP) running on the local computer.


## -struct-fields




### -field dwInDatagrams

The number of datagrams received.


### -field dwNoPorts

The number of datagrams received that were discarded because the port specified was invalid.


### -field dwInErrors

The number of erroneous datagrams  received. This number does not include the value contained by the <b>dwNoPorts</b> member.


### -field dwOutDatagrams

The number of datagrams transmitted.


### -field dwNumAddrs

The number of entries in the UDP listener table.


## -remarks



The 
			<a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-getudpstatistics">GetUdpStatistics</a> function returns a pointer to a <b>MIB_UDPSTATS</b> structure. 

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vistaand later, the organization of header files has changed. This  structure is defined in the <i>Udpmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Udpmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Udpmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcpstatistics">GetTcpStatistics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-getudpstatistics">GetUdpStatistics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/udpmib/ns-udpmib-mib_udprow">MIB_UDPROW</a>
 

 

