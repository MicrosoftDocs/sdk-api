---
UID: NF:pdh.PdhEnumMachinesW
title: PdhEnumMachinesW function (pdh.h)
description: Returns a list of the computer names associated with counters in a log file. (PdhEnumMachinesW)
helpviewer_keywords: ["PdhEnumMachines", "PdhEnumMachines function [Perf]", "PdhEnumMachinesW", "_win32_pdhenummachines", "base.pdhenummachines", "pdh/PdhEnumMachines", "pdh/PdhEnumMachinesW", "perf.pdhenummachines"]
old-location: perf\pdhenummachines.htm
tech.root: perf
ms.assetid: 77584d3b-3ba5-4288-b730-be2458f4fc1c
ms.date: 12/05/2018
ms.keywords: PdhEnumMachines, PdhEnumMachines function [Perf], PdhEnumMachinesA, PdhEnumMachinesW, _win32_pdhenummachines, base.pdhenummachines, pdh/PdhEnumMachines, pdh/PdhEnumMachinesA, pdh/PdhEnumMachinesW, perf.pdhenummachines
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhEnumMachinesW (Unicode) and PdhEnumMachinesA (ANSI)
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
 - PdhEnumMachinesW
 - pdh/PdhEnumMachinesW
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
 - PdhEnumMachines
 - PdhEnumMachinesA
 - PdhEnumMachinesW
---

# PdhEnumMachinesW function


## -description

Returns a list of the computer names associated with counters in a log file. The computer names were either specified when adding counters to the query or when calling the <a href="/windows/desktop/api/pdh/nf-pdh-pdhconnectmachinea">PdhConnectMachine</a> function. The computers listed include those that are currently connected and online, in addition to those that are offline or not returning performance data.
			

To use handles to data sources, use the 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhenummachinesha">PdhEnumMachinesH</a> function.

## -parameters

### -param szDataSource [in]

<b>Null</b>-terminated string that specifies the name of a log file. The function enumerates the names of the computers whose counter data is in the log file. If <b>NULL</b>, the function enumerates the list of computers that were specified when adding counters to a real time query or when calling the <a href="/windows/desktop/api/pdh/nf-pdh-pdhconnectmachinea">PdhConnectMachine</a> function.

### -param mszMachineList [out]

Caller-allocated buffer to receive the list of <b>null</b>-terminated strings that contain the computer names. The list is terminated with two <b>null</b>-terminator characters. Set to <b>NULL</b> if <i>pcchBufferLength</i> is zero.

### -param pcchBufferSize [in, out]

Size of the <i>mszMachineNameList</i> buffer, in <b>TCHARs</b>. If zero on input, the function returns PDH_MORE_DATA and sets this parameter to the required buffer size. If the buffer is larger than the required size, the function sets this parameter to the actual size of the buffer that was used. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

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
The <i>mszMachineNameList</i> buffer is too small to contain all the data. This return value is expected if <i>pcchBufferLength</i> is zero on input. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

</td>
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
</table>

## -remarks

You should call this function twice, the first time to get the required buffer size (set <i>mszMachineNameList</i> to <b>NULL</b> and <i>pcchBufferLength</i> to 0), and the second time to get the data.





> [!NOTE]
> The pdh.h header defines PdhEnumMachines as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhconnectmachinea">PdhConnectMachine</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhenummachinesha">PdhEnumMachinesH</a>
