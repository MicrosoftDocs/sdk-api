---
UID: NF:pdh.PdhRemoveCounter
title: PdhRemoveCounter function (pdh.h)
description: Removes a counter from a query.
helpviewer_keywords: ["PdhRemoveCounter","PdhRemoveCounter function [Perf]","_win32_pdhremovecounter","base.pdhremovecounter","pdh/PdhRemoveCounter","perf.pdhremovecounter"]
old-location: perf\pdhremovecounter.htm
tech.root: perf
ms.assetid: adf9c7bd-47d6-489a-88fc-954fdf127ce8
ms.date: 12/05/2018
ms.keywords: PdhRemoveCounter, PdhRemoveCounter function [Perf], _win32_pdhremovecounter, base.pdhremovecounter, pdh/PdhRemoveCounter, perf.pdhremovecounter
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
 - PdhRemoveCounter
 - pdh/PdhRemoveCounter
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
 - PdhRemoveCounter
---

# PdhRemoveCounter function


## -description

Removes a counter from a query.

## -parameters

### -param hCounter [in]

Handle of the counter to remove from its query. The 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhaddcountera">PdhAddCounter</a> function returns this handle.

## -returns

If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
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
The counter handle is not valid.

</td>
</tr>
</table>

## -remarks

Do not use the counter handle after removing the counter from the query.

The following shows the syntax if calling this function from Visual Basic.


``` syntax
PdhRemoveCounter(
  ByVal CounterHandle as Long  
)
as Long
```


## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhaddcountera">PdhAddCounter</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhopenquerya">PdhOpenQuery</a>
