---
UID: NF:perflib.PerfQueryCounterInfo
title: PerfQueryCounterInfo function
author: windows-sdk-content
description: Gets the counter specifications in the specified query.
old-location: perf\perfquerycounterinfo.htm
old-project: PerfCtrs
ms.assetid: 42CAB98C-4525-499D-BA11-731A666E112D
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PerfQueryCounterInfo, PerfQueryCounterInfo function [Perf], perf.perfquerycounterinfo, perflib/PerfQueryCounterInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: perflib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PerfRegInfoType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	AdvAPI32.dll
api_name:
-	PerfQueryCounterInfo
product: Windows
targetos: Windows
req.lib: AdvAPI32.lib
req.dll: AdvAPI32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PerfQueryCounterInfo function


## -description


Gets the counter specifications in the specified query.


## -parameters




### -param hQuery [in]

A handle to the query for which you want to get the counter specifications


### -param pCounters [out, optional]

Pointer to a buffer that is large enough to hold the amount of data that the <i>cbCounters</i> parameter specifies, in bytes. May be
NULL if <i>cbCounters</i> is 0.


### -param cbCounters

The size of the <i>pCounters</i> buffer, in bytes.


### -param pcbCountersActual [out]

The size of the buffer actually required to get the counter specifications. The meaning depends on the value that the function  

returns.

<table>
<tr>
<th>Function  Return Value</th>
<th>Meaning of <i>pcbCountersActual</i></th>
</tr>
<tr>
<td><b>ERROR_SUCCESS</b></td>
<td>The number of  

  bytes of information about the counter specifications that the function stored in the buffer that <i>pCounters</i> specified.</td>
</tr>
<tr>
<td><b> ERROR_NOT_ENOUGH_MEMORY</b></td>
<td>The  

  size of the buffer required to store the information about the counter specifications, in bytes. Enlarge the buffer to the required  

  size and call the function again.  

</td>
</tr>
<tr>
<td>Other</td>
<td>The value is undefined and should not be used.</td>
</tr>
</table>
 


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function successfully stored all of the information about the counter specifications in the buffer that <i>pCounters</i> specified. The value that <i>pcbCountersActual</i> points to indicates amount of information actually stored in the buffer, in bytes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
 The buffer that <i>pCounters</i> specified was not large enough to store all of the information about the counter specifications.  The value that <i>pcbCountersActual</i> points to  indicates the size of the buffer required to store all of the information. Enlarge the buffer to the required  

  size and call the function again.  



</td>
</tr>
</table>
 


						
						For other types of failures, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. 
					




## -remarks



The information about the counter specifications is written to the buffer that <i>pCounters</i> specifies as a sequence of <a href="https://msdn.microsoft.com/4BBAB831-9A7F-407E-A7D6-9123192C12B4">PERF_COUNTER_IDENTIFIER</a> blocks. The size in bytes of  

the sequence of blocks is written to  <i>pcbCountersActual</i>. Each <b>PERF_COUNTER_IDENTIFIER</b> block consists  

of a <b>PERF_COUNTER_IDENTIFIER</b> structure, optionally followed by a null-terminated UTF-16LE  

instance name, followed by padding so that the size of the  

<b>PERF_COUNTER_IDENTIFIER</b> block is a multiple of 8 bytes. 
 The size of each block, including the <b>PERF_COUNTER_IDENTIFIER</b> structure, instance name,
and padding, is determined by the <b>Size</b> member of the <b>PERF_COUNTER_IDENTIFIER</b> structure, which
will be a multiple of 8 bytes.




## -see-also




<a href="https://msdn.microsoft.com/4BBAB831-9A7F-407E-A7D6-9123192C12B4">PERF_COUNTER_IDENTIFIER</a>
 

 

