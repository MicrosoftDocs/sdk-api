---
UID: NF:pdh.PdhCloseLog
title: PdhCloseLog function (pdh.h)
description: Closes the specified log file.
helpviewer_keywords: ["PDH_FLAGS_CLOSE_QUERY","PdhCloseLog","PdhCloseLog function [Perf]","_win32_pdhcloselog","base.pdhcloselog","pdh/PdhCloseLog","perf.pdhcloselog"]
old-location: perf\pdhcloselog.htm
tech.root: perf
ms.assetid: 74039bdf-d1b5-41ba-aa4e-4779ce0dd02a
ms.date: 12/05/2018
ms.keywords: PDH_FLAGS_CLOSE_QUERY, PdhCloseLog, PdhCloseLog function [Perf], _win32_pdhcloselog, base.pdhcloselog, pdh/PdhCloseLog, perf.pdhcloselog
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
 - PdhCloseLog
 - pdh/PdhCloseLog
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-eventing-pdh-l1-1-3.dll
 - ext-ms-win-eventing-pdh-l1-1-2.dll
 - ext-ms-win-eventing-pdh-l1-1-1.dll
 - ext-ms-win-eventing-pdh-l1-1-0.dll
 - Pdh.dll
api_name:
 - PdhCloseLog
---

# PdhCloseLog function


## -description

Closes the specified log file.

## -parameters

### -param hLog [in]

Handle to the log file to be closed. This handle is returned by the 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhopenloga">PdhOpenLog</a> function.

### -param dwFlags [in]

You can specify the following flag. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PDH_FLAGS_CLOSE_QUERY"></a><a id="pdh_flags_close_query"></a><dl>
<dt><b>PDH_FLAGS_CLOSE_QUERY</b></dt>
</dl>
</td>
<td width="60%">
Closes the query associated with the specified log file handle. See the <i>hQuery</i> parameter of <a href="/windows/desktop/api/pdh/nf-pdh-pdhopenloga">PdhOpenLog</a>.

</td>
</tr>
</table>

## -returns

If the function succeeds, it returns ERROR_SUCCESS and closes and deletes the query.
						

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a> or a 
<a href="/windows/desktop/PerfCtrs/pdh-error-codes">PDH error code</a>. The following is a possible value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The log file handle is not valid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhbindinputdatasourcea">PdhBindInputDataSource</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhopenloga">PdhOpenLog</a>