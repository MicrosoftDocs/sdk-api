---
UID: NS:iprtrmib.MIB_MCAST_LIMIT_ROW
title: MIB_MCAST_LIMIT_ROW (iprtrmib.h)
description: The MIB_MCAST_LIMIT_ROW structure contains the configurable limit information from a corresponding MIB_IPMCAST_IF_ENTRY structure.
helpviewer_keywords: ["*PMIB_MCAST_LIMIT_ROW","MIB_MCAST_LIMIT_ROW","MIB_MCAST_LIMIT_ROW structure [MIB]","PMIB_MCAST_LIMIT_ROW","PMIB_MCAST_LIMIT_ROW structure pointer [MIB]","iprtrmib/MIB_MCAST_LIMIT_ROW","iprtrmib/PMIB_MCAST_LIMIT_ROW","mib.mib_mcast_limit_row"]
old-location: mib\mib_mcast_limit_row.htm
tech.root: MIB
ms.assetid: dc5be2f4-5c6e-43c7-95e8-6a74938ce063
ms.date: 12/05/2018
ms.keywords: '*PMIB_MCAST_LIMIT_ROW, MIB_MCAST_LIMIT_ROW, MIB_MCAST_LIMIT_ROW structure [MIB], PMIB_MCAST_LIMIT_ROW, PMIB_MCAST_LIMIT_ROW structure pointer [MIB], iprtrmib/MIB_MCAST_LIMIT_ROW, iprtrmib/PMIB_MCAST_LIMIT_ROW, mib.mib_mcast_limit_row'
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
req.typenames: MIB_MCAST_LIMIT_ROW, *PMIB_MCAST_LIMIT_ROW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PMIB_MCAST_LIMIT_ROW
 - iprtrmib/PMIB_MCAST_LIMIT_ROW
 - MIB_MCAST_LIMIT_ROW
 - iprtrmib/MIB_MCAST_LIMIT_ROW
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
 - MIB_MCAST_LIMIT_ROW
---

# MIB_MCAST_LIMIT_ROW structure


## -description

The <b>MIB_MCAST_LIMIT_ROW</b> structure contains the configurable limit information from a corresponding <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_if_entry">MIB_IPMCAST_IF_ENTRY</a> structure.

## -struct-fields

### -field dwTtl

The time-to-live value for a multicast interface.

### -field dwRateLimit

The rate limit for a multicast interface.

## -see-also

<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_if_entry">MIB_IPMCAST_IF_ENTRY</a>

