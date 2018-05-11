---
UID: NS:iprtrmib.MIB_MCAST_LIMIT_ROW
title: MIB_MCAST_LIMIT_ROW
author: windows-driver-content
description: The MIB_MCAST_LIMIT_ROW structure contains the configurable limit information from a corresponding MIB_IPMCAST_IF_ENTRY structure.
old-location: mib\mib_mcast_limit_row.htm
old-project: MIB
ms.assetid: dc5be2f4-5c6e-43c7-95e8-6a74938ce063
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: "*PMIB_MCAST_LIMIT_ROW, MIB_MCAST_LIMIT_ROW, MIB_MCAST_LIMIT_ROW structure [MIB], PMIB_MCAST_LIMIT_ROW, PMIB_MCAST_LIMIT_ROW structure pointer [MIB], iprtrmib/MIB_MCAST_LIMIT_ROW, iprtrmib/PMIB_MCAST_LIMIT_ROW, mib.mib_mcast_limit_row"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: MIB_MCAST_LIMIT_ROW, *PMIB_MCAST_LIMIT_ROW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Iprtrmib.h
api_name:
-	MIB_MCAST_LIMIT_ROW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MIB_MCAST_LIMIT_ROW structure


## -description


The <b>MIB_MCAST_LIMIT_ROW</b> structure contains the configurable limit information from a corresponding <a href="https://msdn.microsoft.com/59bc8df1-3999-4acb-b556-e765a9faef79">MIB_IPMCAST_IF_ENTRY</a> structure.


## -struct-fields




### -field dwTtl

The time-to-live value for a multicast interface.


### -field dwRateLimit

The rate limit for a multicast interface.


## -see-also




<a href="https://msdn.microsoft.com/59bc8df1-3999-4acb-b556-e765a9faef79">MIB_IPMCAST_IF_ENTRY</a>
 

 

