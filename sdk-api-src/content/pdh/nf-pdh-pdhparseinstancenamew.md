---
UID: NF:pdh.PdhParseInstanceNameW
title: PdhParseInstanceNameW function (pdh.h)
description: Parses the elements of an instance string. (Unicode)
helpviewer_keywords: ["PdhParseInstanceName", "PdhParseInstanceName function [Perf]", "PdhParseInstanceNameW", "_win32_pdhparseinstancename", "base.pdhparseinstancename", "pdh/PdhParseInstanceName", "pdh/PdhParseInstanceNameW", "perf.pdhparseinstancename"]
old-location: perf\pdhparseinstancename.htm
tech.root: perf
ms.assetid: 8304ecee-5141-450a-be11-838b9f52413b
ms.date: 12/05/2018
ms.keywords: PdhParseInstanceName, PdhParseInstanceName function [Perf], PdhParseInstanceNameA, PdhParseInstanceNameW, _win32_pdhparseinstancename, base.pdhparseinstancename, pdh/PdhParseInstanceName, pdh/PdhParseInstanceNameA, pdh/PdhParseInstanceNameW, perf.pdhparseinstancename
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhParseInstanceNameW (Unicode) and PdhParseInstanceNameA (ANSI)
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
 - PdhParseInstanceNameW
 - pdh/PdhParseInstanceNameW
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
 - PdhParseInstanceName
 - PdhParseInstanceNameA
 - PdhParseInstanceNameW
---

# PdhParseInstanceNameW function


## -description

Parses the elements of an instance string.

## -parameters

### -param szInstanceString [in]

<b>Null</b>-terminated string that specifies the instance string to parse into individual components. This string can contain the following formats, and is less than MAX_PATH characters in length: 




<ul>
<li>instance</li>
<li>instance#index</li>
<li>parent/instance</li>
<li>parent/instance#index</li>
</ul>

### -param szInstanceName [out]

Caller-allocated buffer that receives the <b>null</b>-terminated instance name. Set to <b>NULL</b> if <i>pcchInstanceNameLength</i> is zero.

### -param pcchInstanceNameLength [in, out]

Size of the <i>szInstanceName</i> buffer, in <b>TCHARs</b>. If zero on input, the function returns PDH_MORE_DATA and sets this parameter to the required buffer size. If the buffer is larger than the required size, the function sets this parameter to the actual size of the buffer that was used. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

### -param szParentName [out]

Caller-allocated buffer that receives the <b>null</b>-terminated name of the parent instance, if one is specified. Set to <b>NULL</b> if <i>pcchParentNameLength</i> is zero.

### -param pcchParentNameLength [in, out]

Size of the <i>szParentName</i> buffer, in <b>TCHARs</b>. If zero on input, the function returns PDH_MORE_DATA and sets this parameter to the required buffer size. If the buffer is larger than the required size, the function sets this parameter to the actual size of the buffer that was used. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

### -param lpIndex [out]

Index value of the instance. If an index entry is not present in the string, then this value is zero. This parameter can be <b>NULL</b>.

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
A parameter is not valid. For example, on some releases you could receive this error if the specified size on input is greater than zero but less than the required size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
One or both of the string buffers are too small to contain the data. This return value is expected if the corresponding size buffer  is zero on input. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_INSTANCE</b></dt>
</dl>
</td>
<td width="60%">
The instance string is incorrectly formatted, exceeds MAX_PATH characters in length, or cannot be parsed.

</td>
</tr>
</table>

## -remarks

You should call this function twice, the first time to get the required buffer size (set the buffers to <b>NULL</b> and buffer sizes to 0), and the second time to get the data.





> [!NOTE]
> The pdh.h header defines PdhParseInstanceName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhmakecounterpatha">PdhMakeCounterPath</a>
