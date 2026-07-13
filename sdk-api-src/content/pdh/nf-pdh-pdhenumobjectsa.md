---
UID: NF:pdh.PdhEnumObjectsA
title: PdhEnumObjectsA function (pdh.h)
description: Returns a list of objects available on the specified computer or in the specified log file. To use handles to data sources, use the PdhEnumObjectsH function. (ANSI)
helpviewer_keywords: ["FALSE", "PERF_DETAIL_ADVANCED", "PERF_DETAIL_EXPERT", "PERF_DETAIL_NOVICE", "PERF_DETAIL_WIZARD", "PdhEnumObjectsA", "TRUE", "pdh/PdhEnumObjectsA"]
old-location: perf\pdhenumobjects.htm
tech.root: perf
ms.assetid: dfa4b10f-5134-4620-a6b0-0fa2c13a33ec
ms.date: 12/05/2018
ms.keywords: FALSE, PERF_DETAIL_ADVANCED, PERF_DETAIL_EXPERT, PERF_DETAIL_NOVICE, PERF_DETAIL_WIZARD, PdhEnumObjects, PdhEnumObjects function [Perf], PdhEnumObjectsA, PdhEnumObjectsW, TRUE, _win32_pdhenumobjects, base.pdhenumobjects, pdh/PdhEnumObjects, pdh/PdhEnumObjectsA, pdh/PdhEnumObjectsW, perf.pdhenumobjects
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhEnumObjectsW (Unicode) and PdhEnumObjectsA (ANSI)
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
 - PdhEnumObjectsA
 - pdh/PdhEnumObjectsA
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
 - PdhEnumObjects
 - PdhEnumObjectsA
 - PdhEnumObjectsW
---

# PdhEnumObjectsA function


## -description

Returns a list of objects available on the specified computer or in the specified log file.
			

To use handles to data sources, use the 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhenumobjectsha">PdhEnumObjectsH</a> function.

## -parameters

### -param szDataSource [in]

<b>Null</b>-terminated string that specifies the name of the log file used to enumerate the performance objects. If <b>NULL</b>, the function uses the computer specified in  


the <i>szMachineName</i> parameter to enumerate the names.

### -param szMachineName [in]

<b>Null</b>-terminated string that specifies the name of the computer used to enumerate the performance objects. 


Include the leading slashes in the computer name, for example, \\computername.

If the <i>szDataSource</i> parameter is <b>NULL</b>, you can set <i>szMachineName</i> to <b>NULL</b> to specify the local computer.

### -param mszObjectList [out]

Caller-allocated buffer that receives the list of object names. Each object name in this list is terminated by a <b>null</b> character. The list is terminated with two <b>null</b>-terminator characters. Set to <b>NULL</b> if the <i>pcchBufferLength</i> parameter is zero.

### -param pcchBufferSize [in, out]

Size of the <i>mszObjectList</i> buffer, in <b>TCHARs</b>. If zero on input, the function returns PDH_MORE_DATA and sets this parameter to the required buffer size. If the buffer is larger than the required size, the function sets this parameter to the actual size of the buffer that was used. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

<b>Windows XP:  </b>Add one to the required buffer size.

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

### -param bRefresh [in]

Indicates if the cached object list should be automatically refreshed. Specify one of the following values. 

If you call this function twice, once to get the size of the list and a second time to get the actual list, set this parameter to <b>TRUE</b> on the first call and <b>FALSE</b> on the second call. If both calls are <b>TRUE</b>, the second call may also return PDH_MORE_DATA because the object data may have changed between calls.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The object cache is automatically refreshed before the objects are returned.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Do not automatically refresh the cache.

</td>
</tr>
</table>

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
The <i>mszObjectList</i> buffer is too small to hold the list of objects. This return value is expected if <i>pcchBufferLength</i> is zero on input. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

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
The specified object could not be found.

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
</table>

## -remarks

You should call this function twice, the first time to get the required buffer size (set <i>mszObjectList</i> to <b>NULL</b> and <i>pcchBufferLength</i> to 0), and the second time to get the data.





> [!NOTE]
> The pdh.h header defines PdhEnumObjects as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhenumobjectitemsa">PdhEnumObjectItems</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhenumobjectsha">PdhEnumObjectsH</a>
