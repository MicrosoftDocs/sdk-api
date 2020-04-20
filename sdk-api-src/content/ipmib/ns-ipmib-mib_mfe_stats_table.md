---
UID: NS:ipmib._MIB_MFE_STATS_TABLE
title: MIB_MFE_STATS_TABLE (ipmib.h)
description: Stores statistics for a group of Multicast Forwarding Entries (MFEs).helpviewer_keywords: ["*PMIB_MFE_STATS_TABLE","MIB_MFE_STATS_TABLE","MIB_MFE_STATS_TABLE structure [MIB]","PMIB_MFE_STATS_TABLE","PMIB_MFE_STATS_TABLE structure pointer [MIB]","_mpr_mib_mfe_stats_table","ipmib/MIB_MFE_STATS_TABLE","ipmib/PMIB_MFE_STATS_TABLE","iprtrmib/MIB_MFE_STATS_TABLE","iprtrmib/PMIB_MFE_STATS_TABLE","mib.mib_mfe_stats_table","rras.mib_mfe_stats_table"]
old-location: mib\mib_mfe_stats_table.htm
tech.root: MIB
ms.assetid: d6660e11-7490-4dee-a1d6-980f8a78ac1b
ms.date: 12/05/2018
ms.keywords: '*PMIB_MFE_STATS_TABLE, MIB_MFE_STATS_TABLE, MIB_MFE_STATS_TABLE structure [MIB], PMIB_MFE_STATS_TABLE, PMIB_MFE_STATS_TABLE structure pointer [MIB], _mpr_mib_mfe_stats_table, ipmib/MIB_MFE_STATS_TABLE, ipmib/PMIB_MFE_STATS_TABLE, iprtrmib/MIB_MFE_STATS_TABLE, iprtrmib/PMIB_MFE_STATS_TABLE, mib.mib_mfe_stats_table, rras.mib_mfe_stats_table'
f1_keywords:
- ipmib/MIB_MFE_STATS_TABLE
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Ipmib.h
- Iprtrmib.h
api_name:
- MIB_MFE_STATS_TABLE
targetos: Windows
req.typenames: MIB_MFE_STATS_TABLE, *PMIB_MFE_STATS_TABLE
req.redist: 
ms.custom: 19H1
---

# MIB_MFE_STATS_TABLE structure


## -description


The 
<b>MIB_MFE_STATS_TABLE</b> structure stores statistics for a group of Multicast Forwarding Entries (MFEs).


## -struct-fields




### -field dwNumEntries

The number of MFEs  in the array.


### -field table

A pointer to a table of MFEs that are implemented as an array of 
<a href="https://docs.microsoft.com/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe_stats">MIB_IPMCAST_MFE_STATS</a> structures.


## -remarks



On the Microsoft Windows Software Development Kit (SDK) released for Windows Server 2008and later, the organization of header files has changed. This  structure is defined in the <i>Ipmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe_stats">MIB_IPMCAST_MFE_STATS</a>
 

 

