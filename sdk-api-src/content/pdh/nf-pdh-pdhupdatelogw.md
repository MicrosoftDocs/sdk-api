---
UID: NF:pdh.PdhUpdateLogW
title: PdhUpdateLogW function
author: windows-sdk-content
description: Collects counter data for the current query and writes the data to the log file.
old-location: perf\pdhupdatelog.htm
tech.root: perfctrs
ms.assetid: b2052275-6944-41f4-92ac-38967ed270f3
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: PdhUpdateLog, PdhUpdateLog function [Perf], PdhUpdateLogA, PdhUpdateLogW, _win32_pdhupdatelog, base.pdhupdatelog, pdh/PdhUpdateLog, pdh/PdhUpdateLogA, pdh/PdhUpdateLogW, perf.pdhupdatelog
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
req.unicode-ansi: PdhUpdateLogW (Unicode) and PdhUpdateLogA (ANSI)
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
 - PdhUpdateLog
 - PdhUpdateLogA
 - PdhUpdateLogW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PdhUpdateLogW function


## -description


Collects counter data for the current query and writes the data to the log file.
		


## -parameters




### -param hLog [in]

Handle of a single log file to update. The 
<a href="https://msdn.microsoft.com/a8457959-af3a-497f-91ca-0876cbb552cc">PdhOpenLog</a> function returns this handle.


### -param szUserString [in]

Null-terminated string that contains a user-defined comment to add to the data record. The string can not be empty.


## -returns



If the function succeeds, it returns ERROR_SUCCESS.
						

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
<dt><b>PDH_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The log file handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_ARGUMENT</b></dt>
</dl>
</td>
<td width="60%">
An empty string was passed in the <i>szUserString</i> parameter.

</td>
</tr>
</table>
 




## -remarks



If you are updating a log file from another log file, the comments from the other log file do not migrate.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/a1bc40ea-d928-495a-abc0-daf097202a12">Writing Performance Data to a Log File</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2bb94019-c664-4144-98b6-a0a545f7e4c1">PdhGetLogFileSize</a>



<a href="https://msdn.microsoft.com/a8457959-af3a-497f-91ca-0876cbb552cc">PdhOpenLog</a>



<a href="https://msdn.microsoft.com/ec4e5353-c7f5-4957-b7f4-39df508846a0">PdhOpenQuery</a>



<a href="https://msdn.microsoft.com/e8aa8462-48f1-4ccd-8c41-a7358975e056">PdhUpdateLogFileCatalog</a>
 

 

