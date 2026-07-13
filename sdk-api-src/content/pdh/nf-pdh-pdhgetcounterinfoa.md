---
UID: NF:pdh.PdhGetCounterInfoA
title: PdhGetCounterInfoA function (pdh.h)
description: Retrieves information about a counter, such as data size, counter type, path, and user-supplied data values. (ANSI)
helpviewer_keywords: ["PdhGetCounterInfoA", "pdh/PdhGetCounterInfoA"]
old-location: perf\pdhgetcounterinfo.htm
tech.root: perf
ms.assetid: 12e1a194-5418-4c2a-9853-ef2d2c666893
ms.date: 12/05/2018
ms.keywords: PdhGetCounterInfo, PdhGetCounterInfo function [Perf], PdhGetCounterInfoA, PdhGetCounterInfoW, _win32_pdhgetcounterinfo, base.pdhgetcounterinfo, pdh/PdhGetCounterInfo, pdh/PdhGetCounterInfoA, pdh/PdhGetCounterInfoW, perf.pdhgetcounterinfo
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhGetCounterInfoW (Unicode) and PdhGetCounterInfoA (ANSI)
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
 - PdhGetCounterInfoA
 - pdh/PdhGetCounterInfoA
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
 - PdhGetCounterInfo
 - PdhGetCounterInfoA
 - PdhGetCounterInfoW
---

# PdhGetCounterInfoA function


## -description

Retrieves information about a counter, such as data size, counter type, path, and user-supplied data values.

## -parameters

### -param hCounter [in]

Handle of the counter from which you want to retrieve information. The 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhaddcountera">PdhAddCounter</a> function returns this handle.

### -param bRetrieveExplainText [in]

Determines whether explain text is retrieved. If you set this parameter to <b>TRUE</b>, the explain text for the counter is retrieved. If you set this parameter to <b>FALSE</b>, the field in the returned buffer is <b>NULL</b>.

### -param pdwBufferSize [in, out]

Size of the <i>lpBuffer</i> buffer, in bytes. If zero on input, the function returns PDH_MORE_DATA and sets this parameter to the required buffer size. If the buffer is larger than the required size, the function sets this parameter to the actual size of the buffer that was used. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

### -param lpBuffer [out]

Caller-allocated buffer that receives a 
<a href="/windows/desktop/api/pdh/ns-pdh-pdh_counter_info_a">PDH_COUNTER_INFO</a> structure. The structure is variable-length, because the string data is appended to the end of the fixed-format portion of the structure. This is done so that all data is returned in a single buffer allocated by the caller. Set to <b>NULL</b> if <i>pdwBufferSize</i> is zero.

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
A parameter is not valid or is incorrectly formatted. For example, on some releases you could receive this error if the specified size on input is greater than zero but less than the required size.

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
<tr>
<td width="40%">
<dl>
<dt><b>PDH_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpBuffer</i> buffer is too small to hold the counter information. This return value is expected if <i>pdwBufferSize</i> is zero on input. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

</td>
</tr>
</table>

## -remarks

You should call this function twice, the first time to get the required buffer size (set <i>lpBuffer</i> to <b>NULL</b> and <i>pdwBufferSize</i> to 0), and the second time to get the data.





> [!NOTE]
> The pdh.h header defines PdhGetCounterInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/pdh/ns-pdh-pdh_counter_info_a">PDH_COUNTER_INFO</a>
