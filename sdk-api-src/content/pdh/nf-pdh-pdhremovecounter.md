---
UID: NF:pdh.PdhRemoveCounter
title: PdhRemoveCounter function
author: windows-sdk-content
description: Removes a counter from a query.
old-location: perf\pdhremovecounter.htm
old-project: PerfCtrs
ms.assetid: adf9c7bd-47d6-489a-88fc-954fdf127ce8
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: PdhRemoveCounter, PdhRemoveCounter function [Perf], _win32_pdhremovecounter, base.pdhremovecounter, pdh/PdhRemoveCounter, perf.pdhremovecounter
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
req.unicode-ansi: 
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
 - PdhRemoveCounter
product: Windows
targetos: Windows
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
req.product: ADAM
---

# PdhRemoveCounter function


## -description


Removes a counter from a query.
		


## -parameters




### -param hCounter [in]

Handle of the counter to remove from its query. The 
<a href="https://msdn.microsoft.com/b8b9a332-ce28-46d4-92e2-91f9f6c24da5">PdhAddCounter</a> function returns this handle.


## -returns



If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> or a 
<a href="https://msdn.microsoft.com/ea67d798-81db-44ad-b0fb-24e0c3be7388">PDH error code</a>.


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

<pre class="syntax" xml:space="preserve"><code>PdhRemoveCounter(
  ByVal CounterHandle as Long  
)
as Long</code></pre>





## -see-also




<a href="https://msdn.microsoft.com/b8b9a332-ce28-46d4-92e2-91f9f6c24da5">PdhAddCounter</a>



<a href="https://msdn.microsoft.com/ec4e5353-c7f5-4957-b7f4-39df508846a0">PdhOpenQuery</a>
 

 

