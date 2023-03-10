---
UID: NS:ipmib._MIB_IPMCAST_MFE_STATS_EX_XP
title: MIB_IPMCAST_MFE_STATS_EX_XP (ipmib.h)
description: Stores the extended statistics associated with a Multicast Forwarding Entry (MFE).
helpviewer_keywords: ["*PMIB_IPMCAST_MFE_STATS_EX","*PMIB_IPMCAST_MFE_STATS_EX_XP","MIB_IPMCAST_MFE_STATS_EX","MIB_IPMCAST_MFE_STATS_EX structure [MIB]","MIB_IPMCAST_MFE_STATS_EX_XP","PMIB_IPMCAST_MFE_STATS_EX","PMIB_IPMCAST_MFE_STATS_EX structure pointer [MIB]","ipmib/MIB_IPMCAST_MFE_STATS_EX","ipmib/PMIB_IPMCAST_MFE_STATS_EX","iprtrmib/MIB_IPMCAST_MFE_STATS_EX","iprtrmib/PMIB_IPMCAST_MFE_STATS_EX","mib.mib_ipmcast_mfe_stats_ex"]
old-location: mib\mib_ipmcast_mfe_stats_ex.htm
tech.root: MIB
ms.assetid: 4d1b35bd-da6c-48a1-ade1-f96148c9eecb
ms.date: 12/05/2018
ms.keywords: '*PMIB_IPMCAST_MFE_STATS_EX, *PMIB_IPMCAST_MFE_STATS_EX_XP, MIB_IPMCAST_MFE_STATS_EX, MIB_IPMCAST_MFE_STATS_EX structure [MIB], MIB_IPMCAST_MFE_STATS_EX_XP, PMIB_IPMCAST_MFE_STATS_EX, PMIB_IPMCAST_MFE_STATS_EX structure pointer [MIB], ipmib/MIB_IPMCAST_MFE_STATS_EX, ipmib/PMIB_IPMCAST_MFE_STATS_EX, iprtrmib/MIB_IPMCAST_MFE_STATS_EX, iprtrmib/PMIB_IPMCAST_MFE_STATS_EX, mib.mib_ipmcast_mfe_stats_ex'
req.header: ipmib.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: MIB_IPMCAST_MFE_STATS_EX_XP, *PMIB_IPMCAST_MFE_STATS_EX_XP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IPMCAST_MFE_STATS_EX_XP
 - ipmib/_MIB_IPMCAST_MFE_STATS_EX_XP
 - PMIB_IPMCAST_MFE_STATS_EX_XP
 - ipmib/PMIB_IPMCAST_MFE_STATS_EX_XP
 - MIB_IPMCAST_MFE_STATS_EX_XP
 - ipmib/MIB_IPMCAST_MFE_STATS_EX_XP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipmib.h
 - Iprtrmib.h
api_name:
 - MIB_IPMCAST_MFE_STATS_EX
---

# MIB_IPMCAST_MFE_STATS_EX_XP structure


## -description

The <b>MIB_IPMCAST_MFE_STATS_EX</b> structure stores the extended statistics associated with a Multicast Forwarding Entry (MFE).

## -struct-fields

### -field dwGroup

Type: <b>DWORD</b>

The multicast group for this MFE. A value of zero indicates a wildcard group.

### -field dwSource

Type: <b>DWORD</b>

The range of source addresses for this MFE. A value of zero indicates a wildcard source.

### -field dwSrcMask

Type: <b>DWORD</b>

The IPv4 subnet mask that corresponds to <b>dwSourceAddr</b>. The <b>dwSourceAddr</b> and <b>dwSourceMask</b> members are used together to define a range of sources.

### -field dwUpStrmNgbr

Type: <b>DWORD</b>

The upstream neighbor that is related to this MFE.

### -field dwInIfIndex

Type: <b>DWORD</b>

The index of the incoming interface to which this MFE is related.

### -field dwInIfProtocol

Type: <b>DWORD</b>

The routing protocol that owns the incoming interface to which this MFE is related.

### -field dwRouteProtocol

Type: <b>DWORD</b>

The client that created the route.

### -field dwRouteNetwork

Type: <b>DWORD</b>

The address associated with the route referred to by <b>dwRouteProtocol</b>.

### -field dwRouteMask

Type: <b>DWORD</b>

The mask associated with the route referred to by <b>dwRouteProtocol</b>.

### -field ulUpTime

Type: <b>ULONG</b>

The time, in 100ths of a seconds, since the MFE was created.

### -field ulExpiryTime

Type: <b>ULONG</b>

The time, in 100ths of a seconds, until the MFE will be deleted. Zero is specified if the MFE is not subject to aging requirements.

### -field ulNumOutIf

Type: <b>ULONG</b>

The number of interfaces in the outgoing interface list for this MFE.

### -field ulInPkts

Type: <b>ULONG</b>

The number of packets that have been forwarded that matched this MFE.

### -field ulInOctets

Type: <b>ULONG</b>

The number of octets of data forwarded that match this MFE.

### -field ulPktsDifferentIf

Type: <b>ULONG</b>

The number of packets matching this MFE that were dropped due to an incoming interface check.

### -field ulQueueOverflow

Type: <b>ULONG</b>

The number of packets matching this MFE that were dropped due to a queue overflow. There is one queue per MFE.

### -field ulUninitMfe

Type: <b>ULONG</b>

The number of uninitialized packets that matched this MFE.

### -field ulNegativeMfe

Type: <b>ULONG</b>

The number of packets matching this MFE discarded due to a negative error value.

### -field ulInDiscards

Type: <b>ULONG</b>

The number of discarded forwarded packets that matched this MFE.

### -field ulInHdrErrors

Type: <b>ULONG</b>

The number of packets matching this MFE discarded due to bad or malformed header values (such as a bad Time-to-Live value).

### -field ulTotalOutPackets

Type: <b>ULONG</b>

The total number of MFE packets  transmitted across all associated interfaces. Note that one packet sent over N interfaces will count as N packets within this value.

### -field rgmiosOutStats

## -remarks

The <b>MIB_IPMCAST_MFE_STATS_EX</b> structure extends the functionality of <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe_stats">MIB_IPMCAST_MFE_STATS</a> by including additional information on MFE packets.

This structure does not have a fixed size. Use the <b>SIZEOF_MIB_MFE_STATS_EX(X)</b> macro to determine the size of this structure. This macro is defined in the Iprtrmib.h header file.

The <b>dwRouteProtocol</b>, <b>dwRouteNetwork</b>, and <b>dwRouteMask</b> members uniquely identify the route to which this MFE is related.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed. This  structure is defined in the <i>Ipmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe_stats">MIB_IPMCAST_MFE_STATS</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_mfe_stats_table_ex_xp">MIB_MFE_STATS_TABLE_EX</a>