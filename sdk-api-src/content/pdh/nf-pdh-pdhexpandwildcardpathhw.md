---
UID: NF:pdh.PdhExpandWildCardPathHW
title: PdhExpandWildCardPathHW function
author: windows-sdk-content
description: Examines the specified computer or log file and returns those counter paths that match the given counter path which contains wildcard characters.This function is identical to the PdhExpandWildCardPath function, except that it supports the use of handles to data sources.
old-location: perf\pdhexpandwildcardpathh.htm
tech.root: perfctrs
ms.assetid: d7d13beb-02ab-4204-808e-d395197f09e1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PDH_NOEXPANDCOUNTERS, PDH_NOEXPANDINSTANCES, PdhExpandWildCardPathH, PdhExpandWildCardPathH function [Perf], PdhExpandWildCardPathHA, PdhExpandWildCardPathHW, _win32_pdhexpandwildcardpathh, base.pdhexpandwildcardpathh, pdh/PdhExpandWildCardPathH, pdh/PdhExpandWildCardPathHA, pdh/PdhExpandWildCardPathHW, perf.pdhexpandwildcardpathh
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PdhExpandWildCardPathHW function


## -description


Examines the specified computer or log file and returns those counter paths that match the given counter path which contains wildcard characters.

This function is identical to 
the <a href="https://msdn.microsoft.com/415da310-de56-4d58-8959-231426867526">PdhExpandWildCardPath</a> function, except that it supports the use of handles to data sources.


## -parameters




### -param hDataSource [in]

Handle to a data source returned by the 
<a href="https://msdn.microsoft.com/eaed9b28-eb09-4123-9317-5d3d50e2d77a">PdhBindInputDataSource</a> function.


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
</table>
 


## -returns



If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> or a 
<a href="https://msdn.microsoft.com/ea67d798-81db-44ad-b0fb-24e0c3be7388">PDH error code</a>.

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
<a href="https://msdn.microsoft.com/d90954ab-ec2f-42fd-90b7-66f59f3d1115">PdhExpandCounterPath</a> in the following ways:

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

<b>Prior to Windows Vista:  </b>Partial wildcard matches are not supprted.




## -see-also




<a href="https://msdn.microsoft.com/eaed9b28-eb09-4123-9317-5d3d50e2d77a">PdhBindInputDataSource</a>



<a href="https://msdn.microsoft.com/2cea7d0a-cea2-4fee-a087-37663de254e9">PdhEnumObjectItemsH</a>



<a href="https://msdn.microsoft.com/8f68a7a8-cc56-4f7f-a86f-4b439738808d">PdhEnumObjectsH</a>
 

 

