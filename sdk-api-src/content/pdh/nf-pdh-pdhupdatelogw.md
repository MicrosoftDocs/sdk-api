---
UID: NF:pdh.PdhUpdateLogW
title: PdhUpdateLogW function (pdh.h)
description: Collects counter data for the current query and writes the data to the log file. (Unicode)
helpviewer_keywords: ["PdhUpdateLog", "PdhUpdateLog function [Perf]", "PdhUpdateLogW", "_win32_pdhupdatelog", "base.pdhupdatelog", "pdh/PdhUpdateLog", "pdh/PdhUpdateLogW", "perf.pdhupdatelog"]
old-location: perf\pdhupdatelog.htm
tech.root: perf
ms.assetid: b2052275-6944-41f4-92ac-38967ed270f3
ms.date: 12/05/2018
ms.keywords: PdhUpdateLog, PdhUpdateLog function [Perf], PdhUpdateLogA, PdhUpdateLogW, _win32_pdhupdatelog, base.pdhupdatelog, pdh/PdhUpdateLog, pdh/PdhUpdateLogA, pdh/PdhUpdateLogW, perf.pdhupdatelog
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhUpdateLogW (Unicode) and PdhUpdateLogA (ANSI)
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
 - PdhUpdateLogW
 - pdh/PdhUpdateLogW
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
 - PdhUpdateLog
 - PdhUpdateLogA
 - PdhUpdateLogW
---

# PdhUpdateLogW function


## -description

Collects counter data for the current query and writes the data to the log file.

## -parameters

### -param hLog [in]

Handle of a single log file to update. The 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhopenloga">PdhOpenLog</a> function returns this handle.

### -param szUserString [in]

Null-terminated string that contains a user-defined comment to add to the data record. The string can not be empty.

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
<dt><b>PDH_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The log file handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_ARGUMENT</b></dt>
</dl>
</td>
<td width="60%">
An empty string was passed in the <i>szUserString</i> parameter.

</td>
</tr>
</table>

## -remarks

If you are updating a log file from another log file, the comments from the other log file do not migrate.


#### Examples

For an example, see 
<a href="/windows/desktop/PerfCtrs/writing-performance-data-to-a-log-file">Writing Performance Data to a Log File</a>.

<div class="code"></div>




> [!NOTE]
> The pdh.h header defines PdhUpdateLog as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetlogfilesize">PdhGetLogFileSize</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhopenloga">PdhOpenLog</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhopenquerya">PdhOpenQuery</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhupdatelogfilecatalog">PdhUpdateLogFileCatalog</a>
