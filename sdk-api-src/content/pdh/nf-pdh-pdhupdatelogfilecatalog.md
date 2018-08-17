---
UID: NF:pdh.PdhUpdateLogFileCatalog
title: PdhUpdateLogFileCatalog function
author: windows-sdk-content
description: Synchronizes the information in the log file catalog with the performance data in the log file.
old-location: perf\pdhupdatelogfilecatalog.htm
old-project: perfctrs
ms.assetid: e8aa8462-48f1-4ccd-8c41-a7358975e056
ms.author: windowssdkdev
ms.date: 08/08/2018
ms.keywords: PdhUpdateLogFileCatalog, PdhUpdateLogFileCatalog function [Perf], _win32_pdhupdatelogfilecatalog, base.pdhupdatelogfilecatalog, pdh/PdhUpdateLogFileCatalog, perf.pdhupdatelogfilecatalog
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
 - PdhUpdateLogFileCatalog
product: Windows
targetos: Windows
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
req.product: ADAM
---

# PdhUpdateLogFileCatalog function


## -description


Synchronizes the information in the log file catalog with the performance data in the log file.
		
<div class="alert"><b>Note</b>  This function is obsolete.</div><div> </div>

## -parameters




### -param hLog [in]

Handle to the log file containing the file catalog to update. The 
<a href="https://msdn.microsoft.com/a8457959-af3a-497f-91ca-0876cbb552cc">PdhOpenLog</a> function.


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
<dt><b>PDH_NOT_IMPLEMENTED</b></dt>
</dl>
</td>
<td width="60%">
A handle to a CSV or TSV log file was specified. These log file types do not have catalogs.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_UNKNOWN_LOG_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
A handle to a log file with an unknown format was specified.

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



The log file catalog serves as an index to the performance data records in the log file, providing for faster searches for individual records in the file.

Catalogs should be updated when the data collection process is complete and the log file has been closed. The catalog can be updated during data collection, but doing this may disrupt the process of logging the performance data because updating the catalogs can be time consuming.

Perfmon, CSV, and TSV log files do not have catalogs. Specifying a handle to these log file types will result in a return value of PDH_NOT_IMPLEMENTED.




## -see-also




<a href="https://msdn.microsoft.com/2bb94019-c664-4144-98b6-a0a545f7e4c1">PdhGetLogFileSize</a>



<a href="https://msdn.microsoft.com/b2052275-6944-41f4-92ac-38967ed270f3">PdhUpdateLog</a>
 

 

