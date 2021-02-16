---
UID: NS:pdh._PDH_FMT_COUNTERVALUE
title: PDH_FMT_COUNTERVALUE (pdh.h)
description: The PDH_FMT_COUNTERVALUE structure contains the computed value of the counter and its status.
helpviewer_keywords: ["*PPDH_FMT_COUNTERVALUE","PDH_FMT_COUNTERVALUE","PDH_FMT_COUNTERVALUE structure [Perf]","PPDH_FMT_COUNTERVALUE","PPDH_FMT_COUNTERVALUE structure pointer [Perf]","_win32_pdh_fmt_countervalue_str","base.pdh_fmt_countervalue_str","pdh/PDH_FMT_COUNTERVALUE","pdh/PPDH_FMT_COUNTERVALUE","perf.pdh_fmt_countervalue_str"]
old-location: perf\pdh_fmt_countervalue_str.htm
tech.root: perf
ms.assetid: 68ccd722-94d2-4610-ba64-f51318f5436e
ms.date: 12/05/2018
ms.keywords: '*PPDH_FMT_COUNTERVALUE, PDH_FMT_COUNTERVALUE, PDH_FMT_COUNTERVALUE structure [Perf], PPDH_FMT_COUNTERVALUE, PPDH_FMT_COUNTERVALUE structure pointer [Perf], _win32_pdh_fmt_countervalue_str, base.pdh_fmt_countervalue_str, pdh/PDH_FMT_COUNTERVALUE, pdh/PPDH_FMT_COUNTERVALUE, perf.pdh_fmt_countervalue_str'
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
req.typenames: PDH_FMT_COUNTERVALUE, *PPDH_FMT_COUNTERVALUE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PDH_FMT_COUNTERVALUE
 - pdh/_PDH_FMT_COUNTERVALUE
 - PPDH_FMT_COUNTERVALUE
 - pdh/PPDH_FMT_COUNTERVALUE
 - PDH_FMT_COUNTERVALUE
 - pdh/PDH_FMT_COUNTERVALUE
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
 - PDH_FMT_COUNTERVALUE
---

# PDH_FMT_COUNTERVALUE structure


## -description

The 
<b>PDH_FMT_COUNTERVALUE</b> structure contains the computed value of the counter and its status.

## -struct-fields

### -field CStatus

Counter status that indicates if the counter value is valid. Check this member before using the data in a calculation or displaying its value. For a list of possible values, see 
<a href="/windows/desktop/PerfCtrs/checking-pdh-interface-return-values">Checking PDH Interface Return Values</a>.

### -field longValue

The computed counter value as a <b>LONG</b>.

### -field doubleValue

The computed counter value as a <b>DOUBLE</b>.

### -field largeValue

The computed counter value as a <b>LONGLONG</b>.

### -field AnsiStringValue

The computed counter value as a <b>LPCSTR</b>. Not supported.

### -field WideStringValue

The computed counter value as a <b>LPCWSTR</b>. Not supported.

## -remarks

You specify the data type of the computed counter value when you call <a href="/windows/desktop/api/pdh/nf-pdh-pdhgetformattedcountervalue">PdhGetFormattedCounterValue</a> or <a href="/windows/desktop/api/pdh/nf-pdh-pdhcalculatecounterfromrawvalue">PdhCalculateCounterFromRawValue</a> to compute the counter's value.

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhcalculatecounterfromrawvalue">PdhCalculateCounterFromRawValue</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetformattedcountervalue">PdhGetFormattedCounterValue</a>