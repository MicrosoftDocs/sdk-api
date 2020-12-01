---
UID: NF:pdh.PdhGetLogFileSize
title: PdhGetLogFileSize function (pdh.h)
description: Returns the size of the specified log file.
helpviewer_keywords: ["PdhGetLogFileSize","PdhGetLogFileSize function [Perf]","_win32_pdhgetlogfilesize","base.pdhgetlogfilesize","pdh/PdhGetLogFileSize","perf.pdhgetlogfilesize"]
old-location: perf\pdhgetlogfilesize.htm
tech.root: perf
ms.assetid: 2bb94019-c664-4144-98b6-a0a545f7e4c1
ms.date: 12/05/2018
ms.keywords: PdhGetLogFileSize, PdhGetLogFileSize function [Perf], _win32_pdhgetlogfilesize, base.pdhgetlogfilesize, pdh/PdhGetLogFileSize, perf.pdhgetlogfilesize
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
 - PdhGetLogFileSize
 - pdh/PdhGetLogFileSize
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
 - PdhGetLogFileSize
---

# PdhGetLogFileSize function


## -description

Returns the size of the specified log file.

## -parameters

### -param hLog [in]

Handle to the log file. The 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhopenloga">PdhOpenLog</a> or <a href="/windows/desktop/api/pdh/nf-pdh-pdhbindinputdatasourcea">PdhBindInputDataSource</a> function returns this handle.

### -param llSize [out]

Size of the log file, in bytes.

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
<dt><b>PDH_LOG_FILE_OPEN_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred when trying to open the log file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is not valid.

</td>
</tr>
</table>

## -remarks

If the log file handle points to multiple bound log files, the size is the sum of all the log files. If the log file is a SQL log file, the <i>llSize</i> parameter is the number of records in the log file.

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhopenloga">PdhOpenLog</a>