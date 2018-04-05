---
UID: NS:ipmib._MIB_IPMCAST_OIF_STATS_LH
title: "_MIB_IPMCAST_OIF_STATS_LH"
author: windows-driver-content
description: Stores the statistics that are associated with an outgoing multicast interface.
old-location: mib\mib_ipmcast_oif_stats.htm
old-project: MIB
ms.assetid: 0d1a2396-883b-4ca5-b8a0-11a3d3575a61
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: "*PMIB_IPMCAST_OIF_STATS, *PMIB_IPMCAST_OIF_STATS_LH, MIB_IPMCAST_OIF_STATS, MIB_IPMCAST_OIF_STATS structure [MIB], MIB_IPMCAST_OIF_STATS_LH, PMIB_IPMCAST_OIF_STATS, PMIB_IPMCAST_OIF_STATS structure pointer [MIB], _MIB_IPMCAST_OIF_STATS_LH, _mpr_mib_ipmcast_oif_stats, ipmib/MIB_IPMCAST_OIF_STATS, ipmib/PMIB_IPMCAST_OIF_STATS, iprtrmib/MIB_IPMCAST_OIF_STATS, iprtrmib/PMIB_IPMCAST_OIF_STATS, mib.mib_ipmcast_oif_stats, rras.mib_ipmcast_oif_stats"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ipmib.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: MIB_IPMCAST_OIF_STATS_LH, *PMIB_IPMCAST_OIF_STATS_LH
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ipmib.h
-	Iprtrmib.h
api_name:
-	MIB_IPMCAST_OIF_STATS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MIB_IPMCAST_OIF_STATS_LH structure


## -description


The 
<b>MIB_IPMCAST_OIF_STATS</b> structure stores the statistics that are associated with an outgoing multicast interface.


## -struct-fields




### -field dwOutIfIndex

Type: <b>DWORD</b>

Specifies the outgoing interface to which these statistics are related.


### -field dwNextHopAddr

Type: <b>DWORD</b>

Specifies the address of the next hop that corresponds to <b>dwOutIfIndex</b>. The <b>dwOutIfIndex</b> and <b>dwIfNextHopIPAddr</b> members uniquely identify a next hop on point-to-multipoint interfaces, where one interface connects to multiple networks. Examples of point-to-multipoint interfaces include non-broadcast multiple-access (NBMA) interfaces, and the internal interface on which all dial-up clients connect. 




For Ethernet and other broadcast interfaces, specify zero. Also specify zero for point-to-point interfaces, which are identified by only <b>dwOutIfIndex</b>.


### -field dwDialContext

 


### -field ulTtlTooLow

Type: <b>ULONG</b>

Specifies the number of packets on this outgoing interface that were discarded because the packet's time-to-live (TTL) value was too low.


### -field ulFragNeeded

Type: <b>ULONG</b>

Specifies the number of packets that required fragmentation when they were forwarded on this interface.


### -field ulOutPackets

Type: <b>ULONG</b>

Specifies the number of packets that were forwarded out this interface.


### -field ulOutDiscards

Type: <b>ULONG</b>

Specifies the number of packets that were discarded on this interface.


#### - pvDialContext

Type: <b>PVOID</b>

Reserved. This member should be <b>NULL</b>.


## -remarks



On the Microsoft Windows Software Development Kit (SDK) released for Windows Server 2008
   and later, the organization of header files has changed. This  structure is defined in the <i>Ipmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/4ad35cc0-50e2-47b9-8ce3-9bf8e7032c40">MIB_IPMCAST_OIF</a>
 

 

