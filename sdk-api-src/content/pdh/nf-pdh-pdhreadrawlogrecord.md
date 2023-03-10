---
UID: NF:pdh.PdhReadRawLogRecord
title: PdhReadRawLogRecord function (pdh.h)
description: Reads the information in the specified binary trace log file.
helpviewer_keywords: ["PdhReadRawLogRecord","PdhReadRawLogRecord function [Perf]","_win32_pdhreadrawlogrecord","base.pdhreadrawlogrecord","pdh/PdhReadRawLogRecord","perf.pdhreadrawlogrecord"]
old-location: perf\pdhreadrawlogrecord.htm
tech.root: perf
ms.assetid: fb93b6ea-ca31-4ff1-a553-b02388be8b72
ms.date: 12/05/2018
ms.keywords: PdhReadRawLogRecord, PdhReadRawLogRecord function [Perf], _win32_pdhreadrawlogrecord, base.pdhreadrawlogrecord, pdh/PdhReadRawLogRecord, perf.pdhreadrawlogrecord
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
 - PdhReadRawLogRecord
 - pdh/PdhReadRawLogRecord
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
 - PdhReadRawLogRecord
---

# PdhReadRawLogRecord function


## -description

Reads the information in the specified binary trace log file.

## -parameters

### -param hLog [in]

Handle to the log file. The 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhopenloga">PdhOpenLog</a>  or <a href="/windows/desktop/api/pdh/nf-pdh-pdhbindinputdatasourcea">PdhBindInputDataSource</a> function returns this handle.

### -param ftRecord [in]

Time stamp of the record to be read. If the time stamp does not match a record in the log file, the function returns the record that has a time stamp closest to (but not greater than) the given time stamp.

### -param pRawLogRecord [out]

Caller-allocated buffer that receives a 
<a href="/windows/desktop/api/pdh/ns-pdh-pdh_raw_log_record">PDH_RAW_LOG_RECORD</a> structure; the structure contains the log file record information. Set to <b>NULL</b> if <i>pdwBufferLength</i> is zero.

### -param pdwBufferLength [in]

Size of the <i>pRawLogRecord</i> buffer, in <b>TCHARs</b>. If zero on input, the function returns PDH_MORE_DATA and sets this parameter to the required buffer size. If the buffer is larger than the required size, the function sets this parameter to the actual size of the buffer that was used. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

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
The <i>pRawLogRecord</i> buffer is too small to contain the path elements. This return value is expected if <i>pdwBufferLength</i> is zero on input. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

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

You should call this function twice, the first time to get the required buffer size (set <i>pRawLogRecord</i> to <b>NULL</b> and <i>pdwBufferLength</i> to 0), and the second time to get the data.

## -see-also

<a href="/windows/desktop/api/pdh/ns-pdh-pdh_raw_log_record">PDH_RAW_LOG_RECORD</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhcollectquerydata">PdhCollectQueryData</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhformatfromrawvalue">PdhFormatFromRawValue</a>