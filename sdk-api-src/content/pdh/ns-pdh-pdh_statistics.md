---
UID: NS:pdh._PDH_STATISTICS
title: PDH_STATISTICS (pdh.h)
description: The PDH_STATISTICS structure contains the minimum, maximum, and mean values for an array of raw counters values.
helpviewer_keywords: ["*PPDH_STATISTICS","PDH_STATISTICS","PDH_STATISTICS structure [Perf]","PPDH_STATISTICS","PPDH_STATISTICS structure pointer [Perf]","_win32_pdh_statistics_str","base.pdh_statistics_str","pdh/PDH_STATISTICS","pdh/PPDH_STATISTICS","perf.pdh_statistics_str"]
old-location: perf\pdh_statistics_str.htm
tech.root: perf
ms.assetid: a1daedfd-55f6-418e-b71f-8334cb628d98
ms.date: 12/05/2018
ms.keywords: '*PPDH_STATISTICS, PDH_STATISTICS, PDH_STATISTICS structure [Perf], PPDH_STATISTICS, PPDH_STATISTICS structure pointer [Perf], _win32_pdh_statistics_str, base.pdh_statistics_str, pdh/PDH_STATISTICS, pdh/PPDH_STATISTICS, perf.pdh_statistics_str'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PDH_STATISTICS, *PPDH_STATISTICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PDH_STATISTICS
 - pdh/_PDH_STATISTICS
 - PPDH_STATISTICS
 - pdh/PPDH_STATISTICS
 - PDH_STATISTICS
 - pdh/PDH_STATISTICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pdh.h
api_name:
 - PDH_STATISTICS
---

# PDH_STATISTICS structure


## -description

The 
<b>PDH_STATISTICS</b> structure contains the minimum, maximum, and mean values for an array of raw counters values.

## -struct-fields

### -field dwFormat

Format of the data. The format is specified in the <i>dwFormat</i> when calling 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhcomputecounterstatistics">PdhComputeCounterStatistics</a>.

### -field count

Number of values in the array.

### -field min

Minimum of the values.

### -field max

Maximum of the values.

### -field mean

Mean of the values.

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhcomputecounterstatistics">PdhComputeCounterStatistics</a>