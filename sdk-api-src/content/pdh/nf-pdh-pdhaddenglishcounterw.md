---
UID: NF:pdh.PdhAddEnglishCounterW
title: PdhAddEnglishCounterW function
author: windows-sdk-content
description: Adds the specified language-neutral counter to the query.
old-location: perf\pdhaddenglishcounter.htm
old-project: PerfCtrs
ms.assetid: 6a94b40d-0105-4358-93e1-dae603a35cc4
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PdhAddEnglishCounter, PdhAddEnglishCounter function [Perf], PdhAddEnglishCounterA, PdhAddEnglishCounterW, pdh/PdhAddEnglishCounter, pdh/PdhAddEnglishCounterA, pdh/PdhAddEnglishCounterW, perf.pdhaddenglishcounter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhAddEnglishCounterW (Unicode) and PdhAddEnglishCounterA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CHANNEL_PDU_HEADER, *PCHANNEL_PDU_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Pdh.dll
api_name:
-	PdhAddEnglishCounter
-	PdhAddEnglishCounterA
-	PdhAddEnglishCounterW
product: Windows
targetos: Windows
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PdhAddEnglishCounterW function


## -description


Adds the specified language-neutral counter to the query.
		


## -parameters




### -param hQuery [in]

Handle to the query to which you want to add the counter. This handle is returned by the 
<a href="https://msdn.microsoft.com/ec4e5353-c7f5-4957-b7f4-39df508846a0">PdhOpenQuery</a> function.


### -param szFullCounterPath [in]

Null-terminated string that contains the counter path. For details on the format of a counter path, see 
<a href="https://msdn.microsoft.com/d1f1a90c-425a-4606-b86d-2948305ea84a">Specifying a Counter Path</a>. The maximum length of a counter path is PDH_MAX_COUNTER_PATH.


### -param dwUserData [in]

User-defined value. This value becomes part of the counter information. To retrieve this value later, call the <a href="https://msdn.microsoft.com/12e1a194-5418-4c2a-9853-ef2d2c666893">PdhGetCounterInfo</a> function and access the <b>dwQueryUserData</b> member of the <a href="https://msdn.microsoft.com/c9ede50e-85de-4a68-b539-54285c2599cb">PDH_COUNTER_INFO</a> structure.


### -param phCounter [out]

Handle to the counter that was added to the query. You may need to reference this handle in subsequent calls.


## -returns




						Return ERROR_SUCCESS if the function succeeds.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> or a 
<a href="https://msdn.microsoft.com/ea67d798-81db-44ad-b0fb-24e0c3be7388">PDH error code</a>. The following are possible values.

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
The path did not contain a computer name and the function was unable to retrieve the local computer name. 

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



This function provides a language-neutral way to add performance counters to the query. In contrast, the counter path that you specify in the <a href="https://msdn.microsoft.com/b8b9a332-ce28-46d4-92e2-91f9f6c24da5">PdhAddCounter</a> function must be localized. 

If a counter instance is specified that does not yet exist, 
<b>PdhAddEnglishCounter</b> does not report an error condition. Instead, it returns ERROR_SUCCESS. The reason for this behavior is that it is not known whether a nonexistent counter instance has been specified or whether one will exist but has not yet been created.

To remove the counter from the query, use the 
<a href="https://msdn.microsoft.com/adf9c7bd-47d6-489a-88fc-954fdf127ce8">PdhRemoveCounter</a> function.

<div class="alert"><b>Note</b>  If the counter path contains a wildcard character, the non-wildcard portions of the path will be localized, but wildcards will not be expanded before adding the localized counter path to the query. In this case, you will need use the following procedure to add all matching counter names to the query.  <ol>
<li>Make a query</li>
<li>Use <b>PdhAddEnglishCounter</b> with the string containing wildcards</li>
<li>Use <a href="https://msdn.microsoft.com/12e1a194-5418-4c2a-9853-ef2d2c666893">PdhGetCounterInfo</a> on the counter handle returned by  <b>PdhAddEnglishCounter</b> to get a localized full path (<i>szFullPath</i>.) This string still contains wildcards, but the non-wildcard parts are now localized.
</li>
<li>Use <a href="https://msdn.microsoft.com/415da310-de56-4d58-8959-231426867526">PdhExpandWildCardPath</a> to expand the wildcards.</li>
<li>Use <a href="https://msdn.microsoft.com/b8b9a332-ce28-46d4-92e2-91f9f6c24da5">PdhAddCounter</a> on each of the resulting paths
</li>
</ol>
</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b8b9a332-ce28-46d4-92e2-91f9f6c24da5">PdhAddCounter</a>



<a href="https://msdn.microsoft.com/4e9e4b20-a573-4f6d-97e8-63bcc675032b">PdhBrowseCounters</a>



<a href="https://msdn.microsoft.com/f2dc5f77-9f9e-4290-95fa-ce2f1e81fc69">PdhMakeCounterPath</a>



<a href="https://msdn.microsoft.com/ec4e5353-c7f5-4957-b7f4-39df508846a0">PdhOpenQuery</a>



<a href="https://msdn.microsoft.com/adf9c7bd-47d6-489a-88fc-954fdf127ce8">PdhRemoveCounter</a>
 

 

