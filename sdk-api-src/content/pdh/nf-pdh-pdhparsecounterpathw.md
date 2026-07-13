---
UID: NF:pdh.PdhParseCounterPathW
title: PdhParseCounterPathW function (pdh.h)
description: Parses the elements of the counter path and stores the results in the PDH_COUNTER_PATH_ELEMENTS structure. (Unicode)
helpviewer_keywords: ["PdhParseCounterPath", "PdhParseCounterPath function [Perf]", "PdhParseCounterPathW", "_win32_pdhparsecounterpath", "base.pdhparsecounterpath", "pdh/PdhParseCounterPath", "pdh/PdhParseCounterPathW", "perf.pdhparsecounterpath"]
old-location: perf\pdhparsecounterpath.htm
tech.root: perf
ms.assetid: 760b94e9-88df-4f7d-92e9-333d682779f6
ms.date: 12/05/2018
ms.keywords: PdhParseCounterPath, PdhParseCounterPath function [Perf], PdhParseCounterPathA, PdhParseCounterPathW, _win32_pdhparsecounterpath, base.pdhparsecounterpath, pdh/PdhParseCounterPath, pdh/PdhParseCounterPathA, pdh/PdhParseCounterPathW, perf.pdhparsecounterpath
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhParseCounterPathW (Unicode) and PdhParseCounterPathA (ANSI)
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
 - PdhParseCounterPathW
 - pdh/PdhParseCounterPathW
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
 - PdhParseCounterPath
 - PdhParseCounterPathA
 - PdhParseCounterPathW
---

# PdhParseCounterPathW function


## -description

Parses the elements of the counter path and stores the results in the <a href="/windows/desktop/api/pdh/ns-pdh-pdh_counter_path_elements_a">PDH_COUNTER_PATH_ELEMENTS</a> structure.

## -parameters

### -param szFullPathBuffer [in]

<b>Null</b>-terminated string that contains the counter path to parse. The maximum length of a counter path is PDH_MAX_COUNTER_PATH.

### -param pCounterPathElements [out]

Caller-allocated buffer that receives a 
<a href="/windows/desktop/api/pdh/ns-pdh-pdh_counter_path_elements_a">PDH_COUNTER_PATH_ELEMENTS</a> structure. The structure contains pointers to the individual string elements of the path referenced by the <i>szFullPathBuffer</i> parameter. The function appends the strings to the end of the <b>PDH_COUNTER_PATH_ELEMENTS</b> structure. The allocated buffer should be large enough for the structure and the strings. Set to <b>NULL</b> if <i>pdwBufferSize</i> is zero.

### -param pdwBufferSize [in, out]

Size of the <i>pCounterPathElements</i> buffer, in bytes. If zero on input, the function returns PDH_MORE_DATA and sets this parameter to the required buffer size. If the buffer is larger than the required size, the function sets this parameter to the actual size of the buffer that was used. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

### -param dwFlags

Reserved. Must be zero.

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
A parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The <i>pCounterPathElements</i> buffer is too small to contain the path elements. This return value is expected if <i>pdwBufferSize</i> is zero on input. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_PATH</b></dt>
</dl>
</td>
<td width="60%">
The path is not formatted correctly and cannot be parsed. For example, on some releases you could receive this error if the specified size on input is greater than zero but less than the required size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_MEMORY_ALLOCATION_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
Unable to allocate memory in order to complete the function.

</td>
</tr>
</table>

## -remarks

You should call this function twice, the first time to get the required buffer size (set <i>pCounterPathElements</i> to <b>NULL</b> and <i>pdwBufferSize</i> to 0), and the second time to get the data.





> [!NOTE]
> The pdh.h header defines PdhParseCounterPath as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/pdh/ns-pdh-pdh_counter_path_elements_a">PDH_COUNTER_PATH_ELEMENTS</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhmakecounterpatha">PdhMakeCounterPath</a>
