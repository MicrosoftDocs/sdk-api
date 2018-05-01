---
UID: NS:pdh._PDH_STATISTICS
title: "_PDH_STATISTICS"
author: windows-driver-content
description: The PDH_STATISTICS structure contains the minimum, maximum, and mean values for an array of raw counters values.
old-location: perf\pdh_statistics_str.htm
old-project: PerfCtrs
ms.assetid: a1daedfd-55f6-418e-b71f-8334cb628d98
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: "*PPDH_STATISTICS, PDH_STATISTICS, PDH_STATISTICS structure [Perf], PPDH_STATISTICS, PPDH_STATISTICS structure pointer [Perf], _PDH_STATISTICS, _win32_pdh_statistics_str, base.pdh_statistics_str, pdh/PDH_STATISTICS, pdh/PPDH_STATISTICS, perf.pdh_statistics_str"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PDH_STATISTICS, *PPDH_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Pdh.h
api_name:
-	PDH_STATISTICS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _PDH_STATISTICS structure


## -description



			The 
<b>PDH_STATISTICS</b> structure contains the minimum, maximum, and mean values for an array of raw counters values. 


## -struct-fields




### -field dwFormat

Format of the data. The format is specified in the <i>dwFormat</i> when calling 
<a href="https://msdn.microsoft.com/a986ae6c-88ee-4a03-9077-3d286157b9d1">PdhComputeCounterStatistics</a>.
					


### -field count

Number of values in the array.


### -field min

Minimum of the values.


### -field max

Maximum of the values.


### -field mean

Mean of the values.


## -see-also




<a href="https://msdn.microsoft.com/a986ae6c-88ee-4a03-9077-3d286157b9d1">PdhComputeCounterStatistics</a>
 

 

