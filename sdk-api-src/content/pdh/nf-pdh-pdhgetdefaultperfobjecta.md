---
UID: NF:pdh.PdhGetDefaultPerfObjectA
title: PdhGetDefaultPerfObjectA function (pdh.h)
description: Retrieves the name of the default object. This name can be used to set the initial object selection in the Browse Counter dialog box. To use handles to data sources, use the PdhGetDefaultPerfObjectH function. (ANSI)
helpviewer_keywords: ["PdhGetDefaultPerfObjectA", "pdh/PdhGetDefaultPerfObjectA"]
old-location: perf\pdhgetdefaultperfobject.htm
tech.root: perf
ms.assetid: 7c6d4d82-8b60-4422-8108-8ac10f254278
ms.date: 12/05/2018
ms.keywords: PdhGetDefaultPerfObject, PdhGetDefaultPerfObject function [Perf], PdhGetDefaultPerfObjectA, PdhGetDefaultPerfObjectW, _win32_pdhgetdefaultperfobject, base.pdhgetdefaultperfobject, pdh/PdhGetDefaultPerfObject, pdh/PdhGetDefaultPerfObjectA, pdh/PdhGetDefaultPerfObjectW, perf.pdhgetdefaultperfobject
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhGetDefaultPerfObjectW (Unicode) and PdhGetDefaultPerfObjectA (ANSI)
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
 - PdhGetDefaultPerfObjectA
 - pdh/PdhGetDefaultPerfObjectA
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
 - PdhGetDefaultPerfObject
 - PdhGetDefaultPerfObjectA
 - PdhGetDefaultPerfObjectW
---

# PdhGetDefaultPerfObjectA function


## -description

Retrieves the name of the default object. This name can be used to set the initial object selection in the Browse Counter dialog box.
			

To use handles to data sources, use the 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetdefaultperfobjectha">PdhGetDefaultPerfObjectH</a> function.

## -parameters

### -param szDataSource [in]

Should be <b>NULL</b>. 

If you specify a log file, the <i>szDefaultObjectName</i> parameter will be a <b>null</b> string.

### -param szMachineName [in]

<b>Null</b>-terminated string that specifies the name of the computer used to verify the object name. If <b>NULL</b>, the local computer is used to verify the name.

### -param szDefaultObjectName [out]

Caller-allocated buffer that receives the <b>null</b>-terminated default object name. Set to <b>NULL</b> if the <i>pcchBufferSize</i> parameter is zero.

Note that PDH always returns Processor for the default object name.

### -param pcchBufferSize [in, out]

Size of the <i>szDefaultObjectName</i> buffer, in <b>TCHARs</b>. If zero on input, the function returns PDH_MORE_DATA and sets this parameter to the required buffer size. If the buffer is larger than the required size, the function sets this parameter to the actual size of the buffer that was used. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

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
The <i>szDefaultObjectName</i> buffer is too small to contain the object name. This return value is expected if <i>pcchBufferSize</i> is zero on input. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_ARGUMENT</b></dt>
</dl>
</td>
<td width="60%">
A required parameter is not valid. For example, on some releases you could receive this error if the specified size on input is greater than zero but less than the required size.

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
<tr>
<td width="40%">
<dl>
<dt><b>PDH_CSTATUS_NO_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
The specified computer is offline or unavailable.

</td>
</tr>
</table>

## -remarks

You should call this function twice, the first time to get the required buffer size (set <i>szDefaultObjectName</i> to <b>NULL</b> and <i>pcchBufferSize</i> to 0), and the second time to get the data.





> [!NOTE]
> The pdh.h header defines PdhGetDefaultPerfObject as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetdefaultperfcountera">PdhGetDefaultPerfCounter</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetdefaultperfobjectha">PdhGetDefaultPerfObjectH</a>
