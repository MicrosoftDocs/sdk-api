---
UID: NF:pdh.PdhCloseQuery
title: PdhCloseQuery function (pdh.h)
description: Closes all counters contained in the specified query, closes all handles related to the query, and frees all memory associated with the query.
helpviewer_keywords: ["PdhCloseQuery","PdhCloseQuery function [Perf]","_win32_pdhclosequery","base.pdhclosequery","pdh/PdhCloseQuery","perf.pdhclosequery"]
old-location: perf\pdhclosequery.htm
tech.root: perf
ms.assetid: af0fb9f4-3999-48fa-88d7-aa59b5caed75
ms.date: 12/05/2018
ms.keywords: PdhCloseQuery, PdhCloseQuery function [Perf], _win32_pdhclosequery, base.pdhclosequery, pdh/PdhCloseQuery, perf.pdhclosequery
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
 - PdhCloseQuery
 - pdh/PdhCloseQuery
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
 - PdhCloseQuery
---

# PdhCloseQuery function


## -description

Closes all counters contained in the specified query, closes all handles related to the query, and frees all memory associated with the query.

## -parameters

### -param hQuery [in]

Handle to the query to close. This handle is returned by the 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhopenquerya">PdhOpenQuery</a> function.

## -returns

If the function succeeds, it returns ERROR_SUCCESS. Otherwise, the function returns a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a> or a 
<a href="/windows/desktop/PerfCtrs/pdh-error-codes">PDH error code</a>.
						
					


The following is a possible value.



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
The query handle is not valid.

</td>
</tr>
</table>

## -remarks

Do not use the counter handles associated with this query after calling this function.

The following shows the syntax if calling this function from Visual Basic.


``` syntax
PdhCloseQuery(
  ByVal QueryHandle as Long  
)
as Long
```




#### Examples

For an example, see 
<a href="/windows/desktop/PerfCtrs/browsing-performance-counters">Browsing Performance Counters</a> or 
<a href="/windows/desktop/PerfCtrs/reading-performance-data-from-a-log-file">Reading Performance Data from a Log File</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhopenquerya">PdhOpenQuery</a>
