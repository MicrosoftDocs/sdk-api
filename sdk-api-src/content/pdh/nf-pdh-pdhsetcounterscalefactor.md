---
UID: NF:pdh.PdhSetCounterScaleFactor
title: PdhSetCounterScaleFactor function (pdh.h)
description: Sets the scale factor that is applied to the calculated value of the specified counter when you request the formatted counter value. If the PDH_FMT_NOSCALE flag is set, then this scale factor is ignored.
helpviewer_keywords: ["PdhSetCounterScaleFactor","PdhSetCounterScaleFactor function [Perf]","_win32_pdhsetcounterscalefactor","base.pdhsetcounterscalefactor","pdh/PdhSetCounterScaleFactor","perf.pdhsetcounterscalefactor"]
old-location: perf\pdhsetcounterscalefactor.htm
tech.root: perf
ms.assetid: 6db99e03-0b03-4c1c-b82a-2982b52746db
ms.date: 12/05/2018
ms.keywords: PdhSetCounterScaleFactor, PdhSetCounterScaleFactor function [Perf], _win32_pdhsetcounterscalefactor, base.pdhsetcounterscalefactor, pdh/PdhSetCounterScaleFactor, perf.pdhsetcounterscalefactor
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
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PdhSetCounterScaleFactor
 - pdh/PdhSetCounterScaleFactor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Pdh.dll
api_name:
 - PdhSetCounterScaleFactor
---

# PdhSetCounterScaleFactor function


## -description

Sets the scale factor that is applied to the calculated value of the specified counter when you request the formatted counter value. If the PDH_FMT_NOSCALE flag is set, then this scale factor is ignored.

## -parameters

### -param hCounter [in]

Handle of the counter to apply the scale factor to. The 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhaddcountera">PdhAddCounter</a> function returns this handle.

### -param lFactor [in]

Power of ten by which to multiply the calculated value before returning it. The minimum value of this parameter is PDH_MIN_SCALE (–7), where the returned value is the actual value multiplied by 10<sup>–</sup>⁷. The maximum value of this parameter is PDH_MAX_SCALE (+7), where the returned value is the actual value multiplied by 10⁺⁷. A value of zero will set the scale to one, so that the actual value is returned.

## -returns

If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a> or a 
<a href="/windows/desktop/PerfCtrs/pdh-error-codes">PDH error code</a>. The following are possible values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_ARGUMENT</b></dt>
</dl>
</td>
<td width="60%">
The scale value is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The counter handle is not valid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhcalculatecounterfromrawvalue">PdhCalculateCounterFromRawValue</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhcomputecounterstatistics">PdhComputeCounterStatistics</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetformattedcountervalue">PdhGetFormattedCounterValue</a>