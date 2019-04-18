---
UID: NF:pdh.PdhGetLogFileSize
title: PdhGetLogFileSize function (pdh.h)
author: windows-sdk-content
description: Returns the size of the specified log file.
old-location: perf\pdhgetlogfilesize.htm
tech.root: perfctrs
ms.assetid: 2bb94019-c664-4144-98b6-a0a545f7e4c1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PdhGetLogFileSize, PdhGetLogFileSize function [Perf], _win32_pdhgetlogfilesize, base.pdhgetlogfilesize, pdh/PdhGetLogFileSize, perf.pdhgetlogfilesize
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
 - PdhGetLogFileSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PdhGetLogFileSize function


## -description


Returns the size of the specified log file.
		


## -parameters




### -param hLog [in]

Handle to the log file. The 
<a href="https://msdn.microsoft.com/a8457959-af3a-497f-91ca-0876cbb552cc">PdhOpenLog</a> or <a href="https://msdn.microsoft.com/eaed9b28-eb09-4123-9317-5d3d50e2d77a">PdhBindInputDataSource</a> function returns this handle.


### -param llSize [out]

Size of the log file, in bytes. 


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
<dt><b>PDH_LOG_FILE_OPEN_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred when trying to open the log file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is not valid.

</td>
</tr>
</table>
 




## -remarks



If the log file handle points to multiple bound log files, the size is the sum of all the log files. If the log file is a SQL log file, the <i>llSize</i> parameter is the number of records in the log file.




## -see-also




<a href="https://msdn.microsoft.com/a8457959-af3a-497f-91ca-0876cbb552cc">PdhOpenLog</a>
 

 

