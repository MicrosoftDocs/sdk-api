---
UID: NS:pdh._PDH_RAW_COUNTER
title: PDH_RAW_COUNTER (pdh.h)
description: The PDH_RAW_COUNTER structure returns the data as it was collected from the counter provider. No translation, formatting, or other interpretation is performed on the data.
helpviewer_keywords: ["*PPDH_RAW_COUNTER","PDH_RAW_COUNTER","PDH_RAW_COUNTER structure [Perf]","PPDH_RAW_COUNTER","PPDH_RAW_COUNTER structure pointer [Perf]","_win32_pdh_raw_counter_str","base.pdh_raw_counter_str","pdh/PDH_RAW_COUNTER","pdh/PPDH_RAW_COUNTER","perf.pdh_raw_counter_str"]
old-location: perf\pdh_raw_counter_str.htm
tech.root: perf
ms.assetid: 237a3c82-0ab4-45cb-bd93-2f308178c573
ms.date: 12/05/2018
ms.keywords: '*PPDH_RAW_COUNTER, PDH_RAW_COUNTER, PDH_RAW_COUNTER structure [Perf], PPDH_RAW_COUNTER, PPDH_RAW_COUNTER structure pointer [Perf], _win32_pdh_raw_counter_str, base.pdh_raw_counter_str, pdh/PDH_RAW_COUNTER, pdh/PPDH_RAW_COUNTER, perf.pdh_raw_counter_str'
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
req.typenames: PDH_RAW_COUNTER, *PPDH_RAW_COUNTER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PDH_RAW_COUNTER
 - pdh/_PDH_RAW_COUNTER
 - PPDH_RAW_COUNTER
 - pdh/PPDH_RAW_COUNTER
 - PDH_RAW_COUNTER
 - pdh/PDH_RAW_COUNTER
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
 - PDH_RAW_COUNTER
---

# PDH_RAW_COUNTER structure


## -description

The 
<b>PDH_RAW_COUNTER</b> structure returns the data as it was collected from the counter provider. No translation, formatting, or other interpretation is performed on the data.

## -struct-fields

### -field CStatus

Counter status that indicates if the counter value is valid. Check this member before using the data in a calculation or displaying its value. For a list of possible values, see 
<a href="/windows/desktop/PerfCtrs/checking-pdh-interface-return-values">Checking PDH Interface Return Values</a>.

### -field TimeStamp

Local time for when the data was collected, in 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> format.

### -field FirstValue

First raw counter value.

### -field SecondValue

Second raw counter value. Rate counters require two values in order to compute a displayable value.

### -field MultiCount

If the counter type contains the PERF_MULTI_COUNTER flag, this member contains the additional counter data used in the calculation. For example, the PERF_100NSEC_MULTI_TIMER counter type contains the PERF_MULTI_COUNTER flag.

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhcalculatecounterfromrawvalue">PdhCalculateCounterFromRawValue</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhcomputecounterstatistics">PdhComputeCounterStatistics</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetrawcountervalue">PdhGetRawCounterValue</a>