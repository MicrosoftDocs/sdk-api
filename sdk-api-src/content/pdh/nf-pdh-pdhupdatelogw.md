---
UID: NF:pdh.PdhUpdateLogW
title: PdhUpdateLogW function (pdh.h)
author: windows-sdk-content
description: Collects counter data for the current query and writes the data to the log file.
old-location: perf\pdhupdatelog.htm
tech.root: perfctrs
ms.assetid: b2052275-6944-41f4-92ac-38967ed270f3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PdhUpdateLog, PdhUpdateLog function [Perf], PdhUpdateLogA, PdhUpdateLogW, _win32_pdhupdatelog, base.pdhupdatelog, pdh/PdhUpdateLog, pdh/PdhUpdateLogA, pdh/PdhUpdateLogW, perf.pdhupdatelog
ms.topic: function
f1_keywords: 
 - "pdh/PdhUpdateLog"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Pdh.dll
api_name:
 - PdhUpdateLog
 - PdhUpdateLogA
 - PdhUpdateLogW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PdhUpdateLogW function


## -description


Collects counter data for the current query and writes the data to the log file.
		


## -parameters




### -param hLog [in]

Handle of a single log file to update. The 
<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhopenloga">PdhOpenLog</a> function returns this handle.


### -param szUserString [in]

Null-terminated string that contains a user-defined comment to add to the data record. The string can not be empty.


## -returns



If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a> or a 
<a href="https://docs.microsoft.com/windows/desktop/PerfCtrs/pdh-error-codes">PDH error code</a>. The following are possible values.

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
<a href="https://docs.microsoft.com/windows/desktop/PerfCtrs/writing-performance-data-to-a-log-file">Writing Performance Data to a Log File</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhgetlogfilesize">PdhGetLogFileSize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhopenloga">PdhOpenLog</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhopenquerya">PdhOpenQuery</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhupdatelogfilecatalog">PdhUpdateLogFileCatalog</a>
 

 

