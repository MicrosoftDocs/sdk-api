---
UID: NF:pdh.PdhEnumObjectItemsHW
title: PdhEnumObjectItemsHW function (pdh.h)
description: Returns the specified object's counter and instance names that exist on the specified computer or in the specified log file. This function is identical to the PdhEnumObjectItems function, except that it supports the use of handles to data sources. (Unicode)
helpviewer_keywords: ["PERF_DETAIL_ADVANCED", "PERF_DETAIL_EXPERT", "PERF_DETAIL_NOVICE", "PERF_DETAIL_WIZARD", "PdhEnumObjectItemsH", "PdhEnumObjectItemsH function [Perf]", "PdhEnumObjectItemsHW", "_win32_pdhenumobjectitemsh", "base.pdhenumobjectitemsh", "pdh/PdhEnumObjectItemsH", "pdh/PdhEnumObjectItemsHW", "perf.pdhenumobjectitemsh"]
old-location: perf\pdhenumobjectitemsh.htm
tech.root: perf
ms.assetid: 2cea7d0a-cea2-4fee-a087-37663de254e9
ms.date: 12/05/2018
ms.keywords: PERF_DETAIL_ADVANCED, PERF_DETAIL_EXPERT, PERF_DETAIL_NOVICE, PERF_DETAIL_WIZARD, PdhEnumObjectItemsH, PdhEnumObjectItemsH function [Perf], PdhEnumObjectItemsHA, PdhEnumObjectItemsHW, _win32_pdhenumobjectitemsh, base.pdhenumobjectitemsh, pdh/PdhEnumObjectItemsH, pdh/PdhEnumObjectItemsHA, pdh/PdhEnumObjectItemsHW, perf.pdhenumobjectitemsh
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhEnumObjectItemsHW (Unicode) and PdhEnumObjectItemsHA (ANSI)
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
 - PdhEnumObjectItemsHW
 - pdh/PdhEnumObjectItemsHW
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
 - PdhEnumObjectItemsH
 - PdhEnumObjectItemsHA
 - PdhEnumObjectItemsHW
---

# PdhEnumObjectItemsHW function


## -description

Returns the specified object's counter and instance names that exist on the specified computer or in the specified log file.
			

This function is identical to 
the <a href="/windows/desktop/api/pdh/nf-pdh-pdhenumobjectitemsa">PdhEnumObjectItems</a> function, except that it supports the use of handles to data sources.

## -parameters

### -param hDataSource [in]

Handle to a data source returned by the 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhbindinputdatasourcea">PdhBindInputDataSource</a> function.

### -param szMachineName [in]

<b>Null</b>-terminated string that specifies the name of the computer that contains the counter and instance names that you want to enumerate. 


Include the leading slashes in the computer name, for example, \\computername.

If the <i>szDataSource</i> parameter is <b>NULL</b>, you can set <i>szMachineName</i> to <b>NULL</b> to specify the local computer.

### -param szObjectName [in]

<b>Null</b>-terminated string that specifies the name of the object whose counter and instance names you want to enumerate.

### -param mszCounterList [out]

Caller-allocated buffer that receives a list of <b>null</b>-terminated counter names provided by the specified object. The list contains unique counter names. The list is terminated by two <b>NULL</b> characters. Set to <b>NULL</b> if the <i>pcchCounterListLength</i> parameter is zero.

### -param pcchCounterListLength [in, out]

Size of the <i>mszCounterList</i> buffer, in <b>TCHARs</b>. If zero on input and the object exists, the function returns PDH_MORE_DATA and sets this parameter to the required buffer size. If the buffer is larger than the required size, the function sets this parameter to the actual size of the buffer that was used. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

### -param mszInstanceList [out]

Caller-allocated buffer that receives a list of <b>null</b>-terminated instance names provided by the specified object. The list contains unique instance names. The list is terminated by two <b>NULL</b> characters. Set to <b>NULL</b> if the <i>pcchInstanceListLength</i> parameter is zero.

### -param pcchInstanceListLength [in, out]

Size of the <i>mszInstanceList</i> buffer, in <b>TCHARs</b>. If zero on input and the object exists, the function returns PDH_MORE_DATA and sets this parameter to the required buffer size. If the buffer is larger than the required size, the function sets this parameter to the actual size of the buffer that was used. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

If the specified object does not support variable instances, then the returned value will be zero. If the specified object does support variable instances, but does not currently have any instances, then the value returned is 2, which is the size of an empty MULTI_SZ list string.

### -param dwDetailLevel [in]

Detail level of the performance items to return. All items that are of the specified detail level or less will be returned (the levels are listed in increasing order). This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PERF_DETAIL_NOVICE"></a><a id="perf_detail_novice"></a><dl>
<dt><b>PERF_DETAIL_NOVICE</b></dt>
</dl>
</td>
<td width="60%">
Novice user level of detail.

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_DETAIL_ADVANCED"></a><a id="perf_detail_advanced"></a><dl>
<dt><b>PERF_DETAIL_ADVANCED</b></dt>
</dl>
</td>
<td width="60%">
Advanced user level of detail. 

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_DETAIL_EXPERT"></a><a id="perf_detail_expert"></a><dl>
<dt><b>PERF_DETAIL_EXPERT</b></dt>
</dl>
</td>
<td width="60%">
Expert user level of detail. 

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_DETAIL_WIZARD"></a><a id="perf_detail_wizard"></a><dl>
<dt><b>PERF_DETAIL_WIZARD</b></dt>
</dl>
</td>
<td width="60%">
System designer level of detail. 

</td>
</tr>
</table>

### -param dwFlags [in]

This parameter must be zero.

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
One of the buffers is too small to contain the list of names. This return value is expected if <i>pcchCounterListLength</i> or <i>pcchInstanceListLength</i> is zero on input. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

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
<dt><b>PDH_CSTATUS_NO_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
The specified computer is offline or unavailable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_CSTATUS_NO_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The specified object could not be found on the specified computer or in the specified log file.

</td>
</tr>
</table>

## -remarks

You should call this function twice, the first time to get the required buffer size (set the buffers to <b>NULL</b> and the sizes to 0), and the second time to get the data.

Consecutive calls to this function will return identical lists of counters and instances, because 
<b>PdhEnumObjectItemsH</b> will always query the list of performance objects defined by the last call to 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhenumobjectsha">PdhEnumObjectsH</a> or <b>PdhEnumObjectItemsH</b>. To refresh the list of performance objects, call 
<b>PdhEnumObjectsH</b> with a <i>bRefresh</i> flag value of <b>TRUE</b> before calling 
<b>PdhEnumObjectItemsH</b> again.

The order of the instance and counter names is undetermined.





> [!NOTE]
> The pdh.h header defines PdhEnumObjectItemsH as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhbindinputdatasourcea">PdhBindInputDataSource</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhenumobjectsha">PdhEnumObjectsH</a>
