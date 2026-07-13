---
UID: NF:pdh.PdhExpandWildCardPathHA
title: PdhExpandWildCardPathHA function (pdh.h)
description: Examines the specified computer or log file and returns those counter paths that match the given counter path which contains wildcard characters.This function is identical to the PdhExpandWildCardPath function, except that it supports the use of handles to data sources. (ANSI)
helpviewer_keywords: ["PDH_NOEXPANDCOUNTERS", "PDH_NOEXPANDINSTANCES", "PdhExpandWildCardPathHA", "pdh/PdhExpandWildCardPathHA"]
old-location: perf\pdhexpandwildcardpathh.htm
tech.root: perf
ms.assetid: d7d13beb-02ab-4204-808e-d395197f09e1
ms.date: 08/08/2022
ms.keywords: PDH_NOEXPANDCOUNTERS, PDH_NOEXPANDINSTANCES, PdhExpandWildCardPathH, PdhExpandWildCardPathH function [Perf], PdhExpandWildCardPathHA, PdhExpandWildCardPathHW, _win32_pdhexpandwildcardpathh, base.pdhexpandwildcardpathh, pdh/PdhExpandWildCardPathH, pdh/PdhExpandWildCardPathHA, pdh/PdhExpandWildCardPathHW, perf.pdhexpandwildcardpathh
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhExpandWildCardPathHW (Unicode) and PdhExpandWildCardPathHA (ANSI)
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
 - PdhExpandWildCardPathHA
 - pdh/PdhExpandWildCardPathHA
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
 - PdhExpandWildCardPathH
 - PdhExpandWildCardPathHA
 - PdhExpandWildCardPathHW
---

# PdhExpandWildCardPathHA function


## -description

Examines the specified computer or log file and returns those counter paths that match the given counter path which contains wildcard characters.

This function is identical to 
the <a href="/windows/desktop/api/pdh/nf-pdh-pdhexpandwildcardpatha">PdhExpandWildCardPath</a> function, except that it supports the use of handles to data sources.

## -parameters

### -param hDataSource [in]

Handle to a data source returned by the 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhbindinputdatasourcea">PdhBindInputDataSource</a> function.

### -param szWildCardPath [in]

<b>Null</b>-terminated string that specifies the counter path to expand. The maximum length of a counter path is PDH_MAX_COUNTER_PATH.

If <i>hDataSource</i> is a real time data source, the function searches the computer specified in the path for matches. If the path does not specify a computer, the function searches the local computer.

### -param mszExpandedPathList [out]

Caller-allocated buffer that receives a list of <b>null</b>-terminated counter paths that match the wildcard specification in the <i>szWildCardPath</i>. The list is terminated by two <b>NULL</b> characters. Set to <b>NULL</b> if <i>pcchPathListLength</i> is zero.

### -param pcchPathListLength [in, out]

Size of the <i>mszExpandedPathList</i> buffer, in <b>TCHARs</b>. If zero on input and the object exists, the function returns PDH_MORE_DATA and sets this parameter to the required buffer size. If the buffer is larger than the required size, the function sets this parameter to the actual size of the buffer that was used. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

<div class="alert"><b>Note</b>  You must add one to the required size on Windows XP.</div>
<div> </div>

### -param dwFlags [in]

Flags that indicate which wildcard characters not to expand. You can specify one or more flags. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PDH_NOEXPANDCOUNTERS"></a><a id="pdh_noexpandcounters"></a><dl>
<dt><b>PDH_NOEXPANDCOUNTERS</b></dt>
</dl>
</td>
<td width="60%">
Do not expand the counter name if the path contains a wildcard character for counter name.

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_NOEXPANDINSTANCES"></a><a id="pdh_noexpandinstances"></a><dl>
<dt><b>PDH_NOEXPANDINSTANCES</b></dt>
</dl>
</td>
<td width="60%">
Do not expand the instance name if the path contains a wildcard character for parent instance, instance name, or instance index.

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_REFRESHCOUNTERS"></a><a id="pdh_PDH_REFRESHCOUNTERS"></a><dl>
<dt><b>PDH_REFRESHCOUNTERS</b></dt>
</dl>
</td>
<td width="60%">
Refresh the counter list.
</td>
</tr>
</table>

## -returns

If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a> or a 
<a href="/windows/desktop/PerfCtrs/pdh-error-codes">PDH error code</a>.

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
The <i>mszExpandedPathList</i> buffer is not large enough to contain the list of paths. This return value is expected if <i>pcchPathListLength</i> is zero on input. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

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
<tr>
<td width="40%">
<dl>
<dt><b>PDH_MEMORY_ALLOCATION_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
Unable to allocate memory to support this function.

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
</table>

## -remarks

You should call this function twice, the first time to get the required buffer size (set <i>mszExpandedPathList</i> to <b>NULL</b> and <i>pcchPathListLength</i> to 0), and the second time to get the data.

<b>PdhExpandWildCardPathH</b> differs from 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhexpandcounterpatha">PdhExpandCounterPath</a> in the following ways:

<ol>
<li>Lets you control which wildcard characters are expanded.</li>
<li>The contents of a log file can be used as the source of counter names. </li>
</ol>
The general counter path format is as follows:

\\computer\object(parent/instance#index)\counter

The parent, instance, index, and counter components of the counter path may contain either a valid name or a wildcard character. The computer, parent, instance, and index components are not necessary for all counters.

The following is a list of the possible formats:

<ul>
<li>\\computer\object(parent/instance#index)\counter</li>
<li>\\computer\object(parent/instance)\counter</li>
<li>\\computer\object(instance#index)\counter</li>
<li>\\computer\object(instance)\counter</li>
<li>\\computer\object\counter</li>
<li>\object(parent/instance#index)\counter</li>
<li>\object(parent/instance)\counter</li>
<li>\object(instance#index)\counter</li>
<li>\object(instance)\counter</li>
<li>\object\counter</li>
</ul>
Use an asterisk (*) as the wildcard character, for example, \object(*)\counter.

If a wildcard character is specified in the parent name, all instances of the specified object that match the specified instance and counter fields will be returned. For example, \object(*/instance)\counter.

If a wildcard character is specified in the instance name, all instances of the specified object and parent object will be returned if all instance names corresponding to the specified index match the wildcard character. For example, \object(parent/*)\counter.

If a wildcard character is specified in the counter name, all counters of the specified object are returned.

Partial counter path string matches (for example, "pro*") are  supported.

<b>Prior to Windows Vista:  </b>Partial wildcard matches are not supported.





> [!NOTE]
> The pdh.h header defines PdhExpandWildCardPathH as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

[PdhBindInputDataSourceA function](nf-pdh-pdhbindinputdatasourcea.md)
[PdhEnumObjectItemsHA function](nf-pdh-pdhenumobjectitemsha.md)
[PdhEnumObjectsHA function](nf-pdh-pdhenumobjectsha.md)
[PdhExpandCounterPathA function](nf-pdh-pdhexpandcounterpatha.md)
