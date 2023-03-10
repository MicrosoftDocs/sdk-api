---
UID: NS:iprtrmib._MIB_IPMCAST_BOUNDARY_TABLE
title: MIB_IPMCAST_BOUNDARY_TABLE (iprtrmib.h)
description: Contains a list of a router's scoped IPv4 multicast address boundaries.
helpviewer_keywords: ["*PMIB_IPMCAST_BOUNDARY_TABLE","MIB_IPMCAST_BOUNDARY_TABLE","MIB_IPMCAST_BOUNDARY_TABLE structure [MIB]","PMIB_IPMCAST_BOUNDARY_TABLE","PMIB_IPMCAST_BOUNDARY_TABLE structure pointer [MIB]","iprtrmib/MIB_IPMCAST_BOUNDARY_TABLE","iprtrmib/PMIB_IPMCAST_BOUNDARY_TABLE","mib.mib_ipmcast_boundary_table"]
old-location: mib\mib_ipmcast_boundary_table.htm
tech.root: MIB
ms.assetid: afa93943-efc7-430f-b8d0-4e79132278e2
ms.date: 12/05/2018
ms.keywords: '*PMIB_IPMCAST_BOUNDARY_TABLE, MIB_IPMCAST_BOUNDARY_TABLE, MIB_IPMCAST_BOUNDARY_TABLE structure [MIB], PMIB_IPMCAST_BOUNDARY_TABLE, PMIB_IPMCAST_BOUNDARY_TABLE structure pointer [MIB], iprtrmib/MIB_IPMCAST_BOUNDARY_TABLE, iprtrmib/PMIB_IPMCAST_BOUNDARY_TABLE, mib.mib_ipmcast_boundary_table'
req.header: iprtrmib.h
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
req.typenames: MIB_IPMCAST_BOUNDARY_TABLE, *PMIB_IPMCAST_BOUNDARY_TABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IPMCAST_BOUNDARY_TABLE
 - iprtrmib/_MIB_IPMCAST_BOUNDARY_TABLE
 - PMIB_IPMCAST_BOUNDARY_TABLE
 - iprtrmib/PMIB_IPMCAST_BOUNDARY_TABLE
 - MIB_IPMCAST_BOUNDARY_TABLE
 - iprtrmib/MIB_IPMCAST_BOUNDARY_TABLE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iprtrmib.h
api_name:
 - MIB_IPMCAST_BOUNDARY_TABLE
---

# MIB_IPMCAST_BOUNDARY_TABLE structure


## -description

The <b>MIB_IPMCAST_BOUNDARY_TABLE</b> structure contains a list of  a router's scoped IPv4 multicast address boundaries.

## -struct-fields

### -field dwNumEntries

The number of <a href="/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_ipmcast_boundary">MIB_IPMCAST_BOUNDARY</a> structures listed in <b>table[]</b>.

### -field table

An array of <a href="/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_ipmcast_boundary">MIB_IPMCAST_BOUNDARY</a> structures which collectively define the set of scoped IPv4 multicast address boundaries on a router.

## -remarks

This structure does not have a fixed size. Use the <b>SIZEOF_BOUNDARY_TABLE(X)</b> macro to determine the size of this structure. This macro is defined in the <i>Iprtrmib.h</i> header file.

Note that the <i>Iprtrmib.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Iprtrmib.h</i> header file should never be used directly.

## -see-also

<a href="/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_ipmcast_boundary">MIB_IPMCAST_BOUNDARY</a>