---
UID: NF:pdh.PdhCloseQuery
title: PdhCloseQuery function
author: windows-sdk-content
description: Closes all counters contained in the specified query, closes all handles related to the query, and frees all memory associated with the query.
old-location: perf\pdhclosequery.htm
old-project: perfctrs
ms.assetid: af0fb9f4-3999-48fa-88d7-aa59b5caed75
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: PdhCloseQuery, PdhCloseQuery function [Perf], _win32_pdhclosequery, base.pdhclosequery, pdh/PdhCloseQuery, perf.pdhclosequery
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
 - PdhCloseQuery
product: Windows
targetos: Windows
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
req.product: ADAM
---

# PdhCloseQuery function


## -description


Closes all counters contained in the specified query, closes all handles related to the query, and frees all memory associated with the query.
		


## -parameters




### -param hQuery [in]

Handle to the query to close. This handle is returned by the 
<a href="https://msdn.microsoft.com/ec4e5353-c7f5-4957-b7f4-39df508846a0">PdhOpenQuery</a> function.


## -returns




						If the function succeeds, it returns ERROR_SUCCESS. Otherwise, the function returns a 
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
The query handle is not valid.

</td>
</tr>
</table>
 




## -remarks



Do not use the counter handles associated with this query after calling this function.

The following shows the syntax if calling this function from Visual Basic.

<pre class="syntax" xml:space="preserve"><code>PdhCloseQuery(
  ByVal QueryHandle as Long  
)
as Long</code></pre>



#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/44c5cfa8-6449-45d8-ac30-979b99c086de">Browsing Performance Counters</a> or 
<a href="https://msdn.microsoft.com/acec1506-473a-43c9-9b57-ad8c00e8f250">Reading Performance Data from a Log File</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/ec4e5353-c7f5-4957-b7f4-39df508846a0">PdhOpenQuery</a>
 

 

