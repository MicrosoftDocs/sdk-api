---
UID: NF:pdh.PdhCloseLog
title: PdhCloseLog function
author: windows-sdk-content
description: Closes the specified log file.
old-location: perf\pdhcloselog.htm
tech.root: perfctrs
ms.assetid: 74039bdf-d1b5-41ba-aa4e-4779ce0dd02a
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: PDH_FLAGS_CLOSE_QUERY, PdhCloseLog, PdhCloseLog function [Perf], _win32_pdhcloselog, base.pdhcloselog, pdh/PdhCloseLog, perf.pdhcloselog
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
req.unicode-ansi: 
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
 - PdhCloseLog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PdhCloseLog function


## -description


Closes the specified log file.
		


## -parameters




### -param hLog [in]

Handle to the log file to be closed. This handle is returned by the 
<a href="https://msdn.microsoft.com/a8457959-af3a-497f-91ca-0876cbb552cc">PdhOpenLog</a> function.


### -param dwFlags [in]

You can specify the following flag. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PDH_FLAGS_CLOSE_QUERY"></a><a id="pdh_flags_close_query"></a><dl>
<dt><b>PDH_FLAGS_CLOSE_QUERY</b></dt>
</dl>
</td>
<td width="60%">
Closes the query associated with the specified log file handle. See the <i>hQuery</i> parameter of <a href="https://msdn.microsoft.com/a8457959-af3a-497f-91ca-0876cbb552cc">PdhOpenLog</a>.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, it returns ERROR_SUCCESS and closes and deletes the query.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> or a 
<a href="https://msdn.microsoft.com/ea67d798-81db-44ad-b0fb-24e0c3be7388">PDH error code</a>. The following is a possible value.

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
The log file handle is not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/eaed9b28-eb09-4123-9317-5d3d50e2d77a">PdhBindInputDataSource</a>



<a href="https://msdn.microsoft.com/a8457959-af3a-497f-91ca-0876cbb552cc">PdhOpenLog</a>
 

 

