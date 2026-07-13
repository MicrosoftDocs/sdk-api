---
UID: NF:pdh.PdhEnumLogSetNamesW
title: PdhEnumLogSetNamesW function (pdh.h)
description: Enumerates the names of the log sets within the DSN. (Unicode)
helpviewer_keywords: ["PdhEnumLogSetNames", "PdhEnumLogSetNames function [Perf]", "PdhEnumLogSetNamesW", "_win32_pdhenumlogsetnames", "base.pdhenumlogsetnames", "pdh/PdhEnumLogSetNames", "pdh/PdhEnumLogSetNamesW", "perf.pdhenumlogsetnames"]
old-location: perf\pdhenumlogsetnames.htm
tech.root: perf
ms.assetid: c74cc8a6-915b-40ed-a88b-bc2147215d52
ms.date: 12/05/2018
ms.keywords: PdhEnumLogSetNames, PdhEnumLogSetNames function [Perf], PdhEnumLogSetNamesA, PdhEnumLogSetNamesW, _win32_pdhenumlogsetnames, base.pdhenumlogsetnames, pdh/PdhEnumLogSetNames, pdh/PdhEnumLogSetNamesA, pdh/PdhEnumLogSetNamesW, perf.pdhenumlogsetnames
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhEnumLogSetNamesW (Unicode) and PdhEnumLogSetNamesA (ANSI)
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
 - PdhEnumLogSetNamesW
 - pdh/PdhEnumLogSetNamesW
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
 - PdhEnumLogSetNames
 - PdhEnumLogSetNamesA
 - PdhEnumLogSetNamesW
---

# PdhEnumLogSetNamesW function


## -description

Enumerates the names of the log sets within the DSN.

## -parameters

### -param szDataSource [in]

<b>Null</b>-terminated string that specifies the DSN.

### -param mszDataSetNameList [out]

Caller-allocated buffer that receives the list of <b>null</b>-terminated log set names. The list is terminated with a <b>null</b>-terminator character. Set to <b>NULL</b> if the <i>pcchBufferLength</i> parameter is zero.

### -param pcchBufferLength [in, out]

Size of the <i>mszLogSetNameList</i> buffer, in <b>TCHARs</b>. If zero on input, the function returns PDH_MORE_DATA and sets this parameter to the required buffer size. If the buffer is larger than the required size, the function sets this parameter to the actual size of the buffer that was used. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

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
The size of the <i>mszLogSetNameList</i> buffer is too small to contain all the data. This return value is expected if <i>pcchBufferLength</i> is zero on input. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

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

You should call this function twice, the first time to get the required buffer size (set <i>mszLogSetNameList</i> to <b>NULL</b> and <i>pcchBufferLength</i> to 0), and the second time to get the data.




> [!NOTE]
> The pdh.h header defines PdhEnumLogSetNames as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
