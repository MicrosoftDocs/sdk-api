---
UID: NS:ipmib._MIB_MFE_STATS_TABLE_EX_XP
title: MIB_MFE_STATS_TABLE_EX_XP (ipmib.h)
description: Contains a table of extended statistics for Multicast Forwarding Entries (MFEs).
helpviewer_keywords: ["*PMIB_MFE_STATS_TABLE_EX","*PMIB_MFE_STATS_TABLE_EX_XP","MIB_MFE_STATS_TABLE_EX","MIB_MFE_STATS_TABLE_EX structure [MIB]","MIB_MFE_STATS_TABLE_EX_XP","PMIB_MFE_STATS_TABLE_EX","PMIB_MFE_STATS_TABLE_EX structure pointer [MIB]","ipmib/MIB_MFE_STATS_TABLE_EX","ipmib/PMIB_MFE_STATS_TABLE_EX","iprtrmib/MIB_MFE_STATS_TABLE_EX","iprtrmib/PMIB_MFE_STATS_TABLE_EX","mib.mib_mfe_stats_table_ex"]
old-location: mib\mib_mfe_stats_table_ex.htm
tech.root: MIB
ms.assetid: a13fbca9-b09e-458f-84e5-c8bb6d9fbd19
ms.date: 12/05/2018
ms.keywords: '*PMIB_MFE_STATS_TABLE_EX, *PMIB_MFE_STATS_TABLE_EX_XP, MIB_MFE_STATS_TABLE_EX, MIB_MFE_STATS_TABLE_EX structure [MIB], MIB_MFE_STATS_TABLE_EX_XP, PMIB_MFE_STATS_TABLE_EX, PMIB_MFE_STATS_TABLE_EX structure pointer [MIB], ipmib/MIB_MFE_STATS_TABLE_EX, ipmib/PMIB_MFE_STATS_TABLE_EX, iprtrmib/MIB_MFE_STATS_TABLE_EX, iprtrmib/PMIB_MFE_STATS_TABLE_EX, mib.mib_mfe_stats_table_ex'
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
req.typenames: MIB_MFE_STATS_TABLE_EX_XP, *PMIB_MFE_STATS_TABLE_EX_XP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_MFE_STATS_TABLE_EX_XP
 - ipmib/_MIB_MFE_STATS_TABLE_EX_XP
 - PMIB_MFE_STATS_TABLE_EX_XP
 - ipmib/PMIB_MFE_STATS_TABLE_EX_XP
 - MIB_MFE_STATS_TABLE_EX_XP
 - ipmib/MIB_MFE_STATS_TABLE_EX_XP
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
 - MIB_MFE_STATS_TABLE_EX
---

# MIB_MFE_STATS_TABLE_EX_XP structure


## -description

The <b>MIB_MFE_STATS_TABLE_EX</b> structure contains a table of extended statistics for Multicast Forwarding Entries (MFEs).

## -struct-fields

### -field dwNumEntries

The number of MFEs  in the array.

### -field table

A pointer to a table of MFEs that are implemented as an array of 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe_stats_ex_xp">MIB_IPMCAST_MFE_STATS_EX</a> structures.

## -remarks

On the Microsoft Windows Software Development Kit (SDK) released for Windows Server 2008and later, the organization of header files has changed. This  structure is defined in the <i>Ipmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<b>MIB_IPMCAST_MFE_STATS_EX</b>