---
UID: NF:pdh.PdhMakeCounterPathA
title: PdhMakeCounterPathA function (pdh.h)
description: Creates a full counter path using the members specified in the PDH_COUNTER_PATH_ELEMENTS structure. (ANSI)
helpviewer_keywords: ["0", "PDH_PATH_WBEM_INPUT", "PDH_PATH_WBEM_RESULT", "PdhMakeCounterPathA", "pdh/PdhMakeCounterPathA"]
old-location: perf\pdhmakecounterpath.htm
tech.root: perf
ms.assetid: f2dc5f77-9f9e-4290-95fa-ce2f1e81fc69
ms.date: 12/05/2018
ms.keywords: 0, PDH_PATH_WBEM_INPUT, PDH_PATH_WBEM_RESULT, PdhMakeCounterPath, PdhMakeCounterPath function [Perf], PdhMakeCounterPathA, PdhMakeCounterPathW, _win32_pdhmakecounterpath, base.pdhmakecounterpath, pdh/PdhMakeCounterPath, pdh/PdhMakeCounterPathA, pdh/PdhMakeCounterPathW, perf.pdhmakecounterpath
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhMakeCounterPathW (Unicode) and PdhMakeCounterPathA (ANSI)
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
 - PdhMakeCounterPathA
 - pdh/PdhMakeCounterPathA
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
 - PdhMakeCounterPath
 - PdhMakeCounterPathA
 - PdhMakeCounterPathW
---

# PdhMakeCounterPathA function


## -description

Creates a full counter path using the members specified in the <a href="/windows/desktop/api/pdh/ns-pdh-pdh_counter_path_elements_a">PDH_COUNTER_PATH_ELEMENTS</a> structure.

## -parameters

### -param pCounterPathElements [in]

A 
<a href="/windows/desktop/api/pdh/ns-pdh-pdh_counter_path_elements_a">PDH_COUNTER_PATH_ELEMENTS</a> structure that contains the members used to make up the path. Only the <b>szObjectName</b> and <b>szCounterName</b> members are required, the others are optional. 



If the instance name member is <b>NULL</b>, the path will not contain an instance reference and the <b>szParentInstance</b> and <b>dwInstanceIndex</b> members will be ignored.

### -param szFullPathBuffer [out]

Caller-allocated buffer that receives a <b>null</b>-terminated counter path. The maximum length of a counter path is PDH_MAX_COUNTER_PATH. Set to <b>NULL</b> if <i>pcchBufferSize</i> is zero.

### -param pcchBufferSize [in, out]

Size of the <i>szFullPathBuffer</i> buffer, in <b>TCHARs</b>. If zero on input, the function returns PDH_MORE_DATA and sets this parameter to the required buffer size. If the buffer is larger than the required size, the function sets this parameter to the actual size of the buffer that was used. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

### -param dwFlags [in]

Format of the input and output counter values. You can specify one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PDH_PATH_WBEM_RESULT"></a><a id="pdh_path_wbem_result"></a><dl>
<dt><b>PDH_PATH_WBEM_RESULT</b></dt>
</dl>
</td>
<td width="60%">
 Converts a PDH path to the WMI class and property name format.

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_PATH_WBEM_INPUT"></a><a id="pdh_path_wbem_input"></a><dl>
<dt><b>PDH_PATH_WBEM_INPUT</b></dt>
</dl>
</td>
<td width="60%">
 Converts the WMI class and property name to a PDH path.

</td>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Returns the path in the PDH format, for example, \\computer\object(parent/instance#index)\counter.

</td>
</tr>
</table>

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
<dt><b>PDH_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The <i>szFullPathBuffer</i> buffer is too small to contain the counter name. This return value is expected if <i>pcchBufferSize</i> is zero on input. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

</td>
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
</table>

## -remarks

You should call this function twice, the first time to get the required buffer size (set <i>szFullPathBuffer</i> to <b>NULL</b> and <i>pcchBufferSize</i> to 0), and the second time to get the data.





> [!NOTE]
> The pdh.h header defines PdhMakeCounterPath as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/pdh/ns-pdh-pdh_counter_path_elements_a">PDH_COUNTER_PATH_ELEMENTS</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhparsecounterpatha">PdhParseCounterPath</a>
