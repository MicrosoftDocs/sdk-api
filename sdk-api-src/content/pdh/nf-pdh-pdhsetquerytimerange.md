---
UID: NF:pdh.PdhSetQueryTimeRange
title: PdhSetQueryTimeRange function
author: windows-sdk-content
description: Limits the samples that you can read from a log file to those within the specified time range, inclusively.
old-location: perf\pdhsetquerytimerange.htm
old-project: PerfCtrs
ms.assetid: ed0e100e-9f82-48c0-b4bb-72820c5eeaa8
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PdhSetQueryTimeRange, PdhSetQueryTimeRange function [Perf], _win32_pdhsetquerytimerange, base.pdhsetquerytimerange, pdh/PdhSetQueryTimeRange, perf.pdhsetquerytimerange
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
req.typenames: CHANNEL_PDU_HEADER, *PCHANNEL_PDU_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Pdh.dll
api_name:
-	PdhSetQueryTimeRange
product: Windows
targetos: Windows
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PdhSetQueryTimeRange function


## -description


Limits the samples that you can read from a log file to those within the specified time range, inclusively.


## -parameters




### -param hQuery [in]

Handle to the query. The 
<a href="https://msdn.microsoft.com/ec4e5353-c7f5-4957-b7f4-39df508846a0">PdhOpenQuery</a> function returns this handle.


### -param pInfo [in]

A 
<a href="https://msdn.microsoft.com/a747f288-8d6c-401c-a927-a61ffea3d423">PDH_TIME_INFO</a> structure that specifies the time range. Specify the time as local file time. The end time must be greater than the start time. You can specify 0 for the start time and the maximum 64-bit value for the end time if you want to read all records.


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
The query handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_ARGUMENT</b></dt>
</dl>
</td>
<td width="60%">
The ending time range value must be greater than the starting time range value.

</td>
</tr>
</table>
 




## -remarks



When the end of the specified time range or the end of the log file is reached, the 
<a href="https://msdn.microsoft.com/1d83325b-8deb-4731-9df4-6201da292cdc">PdhCollectQueryData</a> function will return PDH_NO_MORE_DATA.




## -see-also




<a href="https://msdn.microsoft.com/1d83325b-8deb-4731-9df4-6201da292cdc">PdhCollectQueryData</a>



<a href="https://msdn.microsoft.com/142ee829-7f1c-4b97-859c-670f7058dfa1">PdhGetDataSourceTimeRange</a>



<a href="https://msdn.microsoft.com/ec4e5353-c7f5-4957-b7f4-39df508846a0">PdhOpenQuery</a>
 

 

