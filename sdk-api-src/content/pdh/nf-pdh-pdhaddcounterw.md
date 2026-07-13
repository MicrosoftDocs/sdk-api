---
UID: NF:pdh.PdhAddCounterW
title: PdhAddCounterW function (pdh.h)
description: Adds the specified counter to the query. (Unicode)
helpviewer_keywords: ["PdhAddCounter", "PdhAddCounter function [Perf]", "PdhAddCounterW", "_win32_pdhaddcounter", "base.pdhaddcounter", "pdh/PdhAddCounter", "pdh/PdhAddCounterW", "perf.pdhaddcounter"]
old-location: perf\pdhaddcounter.htm
tech.root: perf
ms.assetid: b8b9a332-ce28-46d4-92e2-91f9f6c24da5
ms.date: 12/05/2018
ms.keywords: PdhAddCounter, PdhAddCounter function [Perf], PdhAddCounterA, PdhAddCounterW, _win32_pdhaddcounter, base.pdhaddcounter, pdh/PdhAddCounter, pdh/PdhAddCounterA, pdh/PdhAddCounterW, perf.pdhaddcounter
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhAddCounterW (Unicode) and PdhAddCounterA (ANSI)
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
 - PdhAddCounterW
 - pdh/PdhAddCounterW
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
 - PdhAddCounter
 - PdhAddCounterA
 - PdhAddCounterW
---

# PdhAddCounterW function


## -description

Adds the specified counter to the query.

## -parameters

### -param hQuery [in]

Handle to the query to which you want to add the counter. This handle is returned by the 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhopenquerya">PdhOpenQuery</a> function.

### -param szFullCounterPath [in]

Null-terminated string that contains the counter path. For details on the format of a counter path, see 
<a href="/windows/desktop/PerfCtrs/specifying-a-counter-path">Specifying a Counter Path</a>. The maximum length of a counter path is PDH_MAX_COUNTER_PATH.

### -param dwUserData [in]

User-defined value. This value becomes part of the counter information. To retrieve this value later, call the <a href="/windows/desktop/api/pdh/nf-pdh-pdhgetcounterinfoa">PdhGetCounterInfo</a> function and access the <b>dwUserData</b> member of the <a href="/windows/desktop/api/pdh/ns-pdh-pdh_counter_info_a">PDH_COUNTER_INFO</a> structure.

### -param phCounter [out]

Handle to the counter that was added to the query. You may need to reference this handle in subsequent calls.

## -returns

Return ERROR_SUCCESS if the function succeeds.
						

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
<dt><b>PDH_CSTATUS_BAD_COUNTERNAME</b></dt>
</dl>
</td>
<td width="60%">
The counter path could not be parsed or interpreted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_CSTATUS_NO_COUNTER</b></dt>
</dl>
</td>
<td width="60%">
Unable to find the specified counter on the computer or in the log file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_CSTATUS_NO_COUNTERNAME</b></dt>
</dl>
</td>
<td width="60%">
The counter path is empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_CSTATUS_NO_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
The path did not contain a computer name, and the function was unable to retrieve the local computer name. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_CSTATUS_NO_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
Unable to find the specified object on the computer or in the log file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_FUNCTION_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Unable to determine the calculation function to use for this counter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_ARGUMENT</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
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
<tr>
<td width="40%">
<dl>
<dt><b>PDH_MEMORY_ALLOCATION_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
Unable to allocate memory required to complete the function.

</td>
</tr>
</table>

## -remarks

If the counter path contains a wildcard character, all counter names matching the wildcard character are added to the query.

If a counter instance is specified that does not yet exist, 
<b>PdhAddCounter</b> does not report an error condition. Instead, it returns ERROR_SUCCESS. The reason for this behavior is that it is not known whether a nonexistent counter instance has been specified or whether one will exist but has not yet been created.

To remove the counter from the query, use the 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhremovecounter">PdhRemoveCounter</a> function.


#### Examples

For an example, see 
<a href="/windows/desktop/PerfCtrs/browsing-performance-counters">Browsing Performance Counters</a> or 
<a href="/windows/desktop/PerfCtrs/reading-performance-data-from-a-log-file">Reading Performance Data from a Log File</a>.

<div class="code"></div>




> [!NOTE]
> The pdh.h header defines PdhAddCounter as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhaddenglishcountera">PdhAddEnglishCounter</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhbrowsecountersa">PdhBrowseCounters</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhmakecounterpatha">PdhMakeCounterPath</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhopenquerya">PdhOpenQuery</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhremovecounter">PdhRemoveCounter</a>
