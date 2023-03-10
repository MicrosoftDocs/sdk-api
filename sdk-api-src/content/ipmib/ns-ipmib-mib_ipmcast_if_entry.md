---
UID: NS:ipmib._MIB_IPMCAST_IF_ENTRY
title: MIB_IPMCAST_IF_ENTRY (ipmib.h)
description: Stores information about an IP multicast interface.
helpviewer_keywords: ["*PMIB_IPMCAST_IF_ENTRY","MIB_IPMCAST_IF_ENTRY","MIB_IPMCAST_IF_ENTRY structure [MIB]","PMIB_IPMCAST_IF_ENTRY","PMIB_IPMCAST_IF_ENTRY structure pointer [MIB]","_mpr_mib_ipmcast_if_entry","ipmib/MIB_IPMCAST_IF_ENTRY","ipmib/PMIB_IPMCAST_IF_ENTRY","iprtrmib/MIB_IPMCAST_IF_ENTRY","iprtrmib/PMIB_IPMCAST_IF_ENTRY","mib.mib_ipmcast_if_entry","rras.mib_ipmcast_if_entry"]
old-location: mib\mib_ipmcast_if_entry.htm
tech.root: MIB
ms.assetid: 59bc8df1-3999-4acb-b556-e765a9faef79
ms.date: 12/05/2018
ms.keywords: '*PMIB_IPMCAST_IF_ENTRY, MIB_IPMCAST_IF_ENTRY, MIB_IPMCAST_IF_ENTRY structure [MIB], PMIB_IPMCAST_IF_ENTRY, PMIB_IPMCAST_IF_ENTRY structure pointer [MIB], _mpr_mib_ipmcast_if_entry, ipmib/MIB_IPMCAST_IF_ENTRY, ipmib/PMIB_IPMCAST_IF_ENTRY, iprtrmib/MIB_IPMCAST_IF_ENTRY, iprtrmib/PMIB_IPMCAST_IF_ENTRY, mib.mib_ipmcast_if_entry, rras.mib_ipmcast_if_entry'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MIB_IPMCAST_IF_ENTRY, *PMIB_IPMCAST_IF_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IPMCAST_IF_ENTRY
 - ipmib/_MIB_IPMCAST_IF_ENTRY
 - PMIB_IPMCAST_IF_ENTRY
 - ipmib/PMIB_IPMCAST_IF_ENTRY
 - MIB_IPMCAST_IF_ENTRY
 - ipmib/MIB_IPMCAST_IF_ENTRY
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
 - MIB_IPMCAST_IF_ENTRY
---

# MIB_IPMCAST_IF_ENTRY structure


## -description

The 
<b>MIB_IPMCAST_IF_ENTRY</b> structure stores information about an IP multicast interface.

## -struct-fields

### -field dwIfIndex

The index of this interface.

### -field dwTtl

The time-to-live value for this interface.

### -field dwProtocol

The multicast routing protocol that owns this interface.

### -field dwRateLimit

The rate limit of this interface.

### -field ulInMcastOctets

The number of octets of multicast data received through this interface.

### -field ulOutMcastOctets

The number of octets of multicast data sent through this interface.

## -remarks

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed. This  structure is defined in the <i>Ipmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_if_table">MIB_IPMCAST_IF_TABLE</a>