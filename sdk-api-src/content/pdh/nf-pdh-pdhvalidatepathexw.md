---
UID: NF:pdh.PdhValidatePathExW
title: PdhValidatePathExW function (pdh.h)
description: Validates that the specified counter is present on the computer or in the log file. (Unicode)
helpviewer_keywords: ["PdhValidatePathEx", "PdhValidatePathEx function [Perf]", "PdhValidatePathExW", "pdh/PdhValidatePathEx", "pdh/PdhValidatePathExW", "perf.pdhvalidatepathex"]
old-location: perf\pdhvalidatepathex.htm
tech.root: perf
ms.assetid: e6b52af7-7276-4565-aa61-73899796a13c
ms.date: 12/05/2018
ms.keywords: PdhValidatePathEx, PdhValidatePathEx function [Perf], PdhValidatePathExA, PdhValidatePathExW, pdh/PdhValidatePathEx, pdh/PdhValidatePathExA, pdh/PdhValidatePathExW, perf.pdhvalidatepathex
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhValidatePathExW (Unicode) and PdhValidatePathExA (ANSI)
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
 - PdhValidatePathExW
 - pdh/PdhValidatePathExW
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
 - PdhValidatePathEx
 - PdhValidatePathExA
 - PdhValidatePathExW
---

# PdhValidatePathExW function


## -description

Validates that the specified counter is present on the computer or in the log file.

## -parameters

### -param hDataSource [in, optional]

Handle to the data source. The <a href="/windows/desktop/api/pdh/nf-pdh-pdhopenloga">PdhOpenLog</a> and <a href="/windows/desktop/api/pdh/nf-pdh-pdhbindinputdatasourcea">PdhBindInputDataSource</a> functions return this handle. 

To validate that the counter is present on the local computer, specify <b>NULL</b> (this is the same as calling <a href="/windows/desktop/api/pdh/nf-pdh-pdhvalidatepatha">PdhValidatePath</a>).

### -param szFullPathBuffer [in]

<b>Null</b>-terminated string that specifies the counter path to validate. The maximum length of a counter path is PDH_MAX_COUNTER_PATH.

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
<dt><b>PDH_CSTATUS_NO_INSTANCE</b></dt>
</dl>
</td>
<td width="60%">
The specified instance of the performance object was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_CSTATUS_NO_COUNTER</b></dt>
</dl>
</td>
<td width="60%">
The specified counter was not found in the performance object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_CSTATUS_NO_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The specified performance object was not found on the computer or in the log file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_CSTATUS_NO_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
The specified computer could not be found or connected to.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_CSTATUS_BAD_COUNTERNAME</b></dt>
</dl>
</td>
<td width="60%">
The counter path string could not be parsed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_MEMORY_ALLOCATION_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The function is unable to allocate a required temporary buffer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhmakecounterpatha">PdhMakeCounterPath</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhvalidatepatha">PdhValidatePath</a>

## -remarks

> [!NOTE]
> The pdh.h header defines PdhValidatePathEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
