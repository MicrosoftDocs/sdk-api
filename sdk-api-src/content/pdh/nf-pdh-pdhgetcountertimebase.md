---
UID: NF:pdh.PdhGetCounterTimeBase
title: PdhGetCounterTimeBase function (pdh.h)
description: Returns the time base of the specified counter.
helpviewer_keywords: ["PdhGetCounterTimeBase","PdhGetCounterTimeBase function [Perf]","_win32_pdhgetcountertimebase","base.pdhgetcountertimebase","pdh/PdhGetCounterTimeBase","perf.pdhgetcountertimebase"]
old-location: perf\pdhgetcountertimebase.htm
tech.root: perf
ms.assetid: b034c00e-50f1-46af-aebc-0cb968c0b737
ms.date: 12/05/2018
ms.keywords: PdhGetCounterTimeBase, PdhGetCounterTimeBase function [Perf], _win32_pdhgetcountertimebase, base.pdhgetcountertimebase, pdh/PdhGetCounterTimeBase, perf.pdhgetcountertimebase
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
 - PdhGetCounterTimeBase
 - pdh/PdhGetCounterTimeBase
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
 - PdhGetCounterTimeBase
---

# PdhGetCounterTimeBase function


## -description

Returns the time base of the specified counter.

## -parameters

### -param hCounter [in]

Handle to the counter. The 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhaddcountera">PdhAddCounter</a> function returns this handle.

### -param pTimeBase [out]

Time base that specifies the number of performance values a counter samples per second.

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
The specified counter does not use a time base.

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

## -remarks

If you use 
			the 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhformatfromrawvalue">PdhFormatFromRawValue</a> function to calculate a displayable value instead of calling the <a href="/windows/desktop/api/pdh/nf-pdh-pdhcalculatecounterfromrawvalue">PdhCalculateCounterFromRawValue</a> function, you must call the 
<b>PdhGetCounterTimeBase</b> function to retrieve the time base.
		

Each counter that returns time-based performance data has a time base defined for it. The time base of a counter is the number of times a counter samples data per second.

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhformatfromrawvalue">PdhFormatFromRawValue</a>