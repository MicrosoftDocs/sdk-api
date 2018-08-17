---
UID: NF:pdh.PdhAddCounterA
title: PdhAddCounterA function
author: windows-sdk-content
description: Adds the specified counter to the query.
old-location: perf\pdhaddcounter.htm
old-project: perfctrs
ms.assetid: b8b9a332-ce28-46d4-92e2-91f9f6c24da5
ms.author: windowssdkdev
ms.date: 08/08/2018
ms.keywords: PdhAddCounter, PdhAddCounter function [Perf], PdhAddCounterA, PdhAddCounterW, _win32_pdhaddcounter, base.pdhaddcounter, pdh/PdhAddCounter, pdh/PdhAddCounterA, pdh/PdhAddCounterW, perf.pdhaddcounter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: pdh.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: CHANNEL_PDU_HEADER, *PCHANNEL_PDU_HEADER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Pdh.dll
api_name:
 - PdhAddCounter
 - PdhAddCounterA
 - PdhAddCounterW
product: Windows
targetos: Windows
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
req.product: ADAM
---

# PdhAddCounterA function


## -description


Adds the specified counter to the query.
		


## -parameters




### -param hQuery [in]

Handle to the query to which you want to add the counter. This handle is returned by the 
<a href="https://msdn.microsoft.com/ec4e5353-c7f5-4957-b7f4-39df508846a0">PdhOpenQuery</a> function.


### -param szFullCounterPath [in]

Null-terminated string that contains the counter path. For details on the format of a counter path, see 
<a href="https://msdn.microsoft.com/d1f1a90c-425a-4606-b86d-2948305ea84a">Specifying a Counter Path</a>. The maximum length of a counter path is PDH_MAX_COUNTER_PATH.


### -param dwUserData [in]

User-defined value. This value becomes part of the counter information. To retrieve this value later, call the <a href="https://msdn.microsoft.com/12e1a194-5418-4c2a-9853-ef2d2c666893">PdhGetCounterInfo</a> function and access the <b>dwUserData</b> member of the <a href="https://msdn.microsoft.com/c9ede50e-85de-4a68-b539-54285c2599cb">PDH_COUNTER_INFO</a> structure.


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
<a href="https://msdn.microsoft.com/adf9c7bd-47d6-489a-88fc-954fdf127ce8">PdhRemoveCounter</a> function.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/44c5cfa8-6449-45d8-ac30-979b99c086de">Browsing Performance Counters</a> or 
<a href="https://msdn.microsoft.com/acec1506-473a-43c9-9b57-ad8c00e8f250">Reading Performance Data from a Log File</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/6a94b40d-0105-4358-93e1-dae603a35cc4">PdhAddEnglishCounter</a>



<a href="https://msdn.microsoft.com/4e9e4b20-a573-4f6d-97e8-63bcc675032b">PdhBrowseCounters</a>



<a href="https://msdn.microsoft.com/f2dc5f77-9f9e-4290-95fa-ce2f1e81fc69">PdhMakeCounterPath</a>



<a href="https://msdn.microsoft.com/ec4e5353-c7f5-4957-b7f4-39df508846a0">PdhOpenQuery</a>



<a href="https://msdn.microsoft.com/adf9c7bd-47d6-489a-88fc-954fdf127ce8">PdhRemoveCounter</a>
 

 

