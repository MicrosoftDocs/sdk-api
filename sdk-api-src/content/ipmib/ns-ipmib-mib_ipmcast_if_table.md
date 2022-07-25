---
UID: NS:ipmib._MIB_IPMCAST_IF_TABLE
title: MIB_IPMCAST_IF_TABLE (ipmib.h)
description: Contains a table of IP multicast interface entries.
helpviewer_keywords: ["*PMIB_IPMCAST_IF_TABLE","MIB_IPMCAST_IF_TABLE","MIB_IPMCAST_IF_TABLE structure [MIB]","PMIB_IPMCAST_IF_TABLE","PMIB_IPMCAST_IF_TABLE structure pointer [MIB]","_mpr_mib_ipmcast_if_table","ipmib/MIB_IPMCAST_IF_TABLE","ipmib/PMIB_IPMCAST_IF_TABLE","iprtrmib/MIB_IPMCAST_IF_TABLE","iprtrmib/PMIB_IPMCAST_IF_TABLE","mib.mib_ipmcast_if_table","rras.mib_ipmcast_if_table"]
old-location: mib\mib_ipmcast_if_table.htm
tech.root: MIB
ms.assetid: 6ea374e3-cb09-44e5-b80a-b68447589191
ms.date: 12/05/2018
ms.keywords: '*PMIB_IPMCAST_IF_TABLE, MIB_IPMCAST_IF_TABLE, MIB_IPMCAST_IF_TABLE structure [MIB], PMIB_IPMCAST_IF_TABLE, PMIB_IPMCAST_IF_TABLE structure pointer [MIB], _mpr_mib_ipmcast_if_table, ipmib/MIB_IPMCAST_IF_TABLE, ipmib/PMIB_IPMCAST_IF_TABLE, iprtrmib/MIB_IPMCAST_IF_TABLE, iprtrmib/PMIB_IPMCAST_IF_TABLE, mib.mib_ipmcast_if_table, rras.mib_ipmcast_if_table'
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
req.typenames: MIB_IPMCAST_IF_TABLE, *PMIB_IPMCAST_IF_TABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IPMCAST_IF_TABLE
 - ipmib/_MIB_IPMCAST_IF_TABLE
 - PMIB_IPMCAST_IF_TABLE
 - ipmib/PMIB_IPMCAST_IF_TABLE
 - MIB_IPMCAST_IF_TABLE
 - ipmib/MIB_IPMCAST_IF_TABLE
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
 - MIB_IPMCAST_IF_TABLE
---

# MIB_IPMCAST_IF_TABLE structure


## -description

The 
<b>MIB_IPMCAST_IF_TABLE</b> structure contains a table of IP multicast interface entries.

## -struct-fields

### -field dwNumEntries

Specifies the number of interface entries in the table.

### -field table

A pointer to a table of interface entries implemented as an array of 
<b>MIB_IPMCAST_IF_TABLE</b> structures.

## -remarks

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed. This  structure is defined in the <i>Ipmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_if_entry">MIB_IPMCAST_IF_ENTRY</a>