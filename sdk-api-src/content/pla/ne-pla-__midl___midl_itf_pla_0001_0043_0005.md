---
UID: NE:pla.__MIDL___MIDL_itf_pla_0001_0043_0005
title: "__MIDL___MIDL_itf_pla_0001_0043_0005"
author: windows-driver-content
description: Defines the clock resolution to use when tracing events.
old-location: pla\clocktype.htm
old-project: PLA
ms.assetid: e255d486-2f1f-4a3d-a8a5-1c997d61a073
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ClockType, ClockType enumeration [PLA], __MIDL___MIDL_itf_pla_0001_0043_0005, base.clocktype, pla.clocktype, pla/ClockType, pla/plaCycle, pla/plaPerformance, pla/plaSystem, pla/plaTimeStamp, plaCycle, plaPerformance, plaSystem, plaTimeStamp
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ClockType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Pla.h
api_name:
-	ClockType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# __MIDL___MIDL_itf_pla_0001_0043_0005 enumeration


## -description


Defines the clock resolution to use when tracing events.


## -enum-fields




### -field plaTimeStamp

Use the raw (unconverted) time stamp.


### -field plaPerformance

Query performance counter. This counter provides a high-resolution (100 nanoseconds) time stamp but is more resource-intensive to retrieve than  system time.


### -field plaSystem

System time. The system time provides a low-resolution (10 milliseconds) time stamp but is less resource-intensive to retrieve than the query performance counter. 


### -field plaCycle

CPU cycle counter. The CPU counter provides the highest resolution time stamp and is the least resource-intensive to retrieve. However, the CPU counter is unreliable and should not be used in production. 


## -remarks



For details, see the <b>ClientContext</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566375">WNODE_HEADER</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/8c62d441-01c5-4fca-a802-41c7328a22e9">ITraceDataCollector::ClockType</a>
 

 

