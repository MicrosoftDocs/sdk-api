---
UID: NF:pdh.PdhCollectQueryDataWithTime
title: PdhCollectQueryDataWithTime function
author: windows-sdk-content
description: Collects the current raw data value for all counters in the specified query and updates the status code of each counter.
old-location: perf\pdhcollectquerydatawithtime.htm
tech.root: perfctrs
ms.assetid: 2c47c690-0748-4ed4-a138-894d45c72581
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: PdhCollectQueryDataWithTime, PdhCollectQueryDataWithTime function [Perf], base.pdhcollectquerydatawithtime, pdh/PdhCollectQueryDataWithTime, perf.pdhcollectquerydatawithtime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - PdhCollectQueryDataWithTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PdhCollectQueryDataWithTime function


## -description


Collects the current raw data value for all counters in the specified query and updates the status code of each counter.
		


## -parameters




### -param hQuery [in, out]

Handle of the query for which you want to collect data. The <a href="https://msdn.microsoft.com/ec4e5353-c7f5-4957-b7f4-39df508846a0">PdhOpenQuery</a> function returns this handle.


### -param pllTimeStamp [out]

Time stamp when the first counter value in the query was retrieved. The time is specified as FILETIME.


## -returns



If the function succeeds, it returns ERROR_SUCCESS. Otherwise, the function returns a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> or a 
<a href="https://msdn.microsoft.com/ea67d798-81db-44ad-b0fb-24e0c3be7388">PDH error code</a>.
						
					


The following are possible values.



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
<dt><b>PDH_NO_DATA</b></dt>
</dl>
</td>
<td width="60%">
The query does not currently have any counters.

</td>
</tr>
</table>
 




## -remarks



Call this function when you want to collect counter data for the counters in the query. PDH stores the raw counter values for the current and previous collection. 

If you want to retrieve the current raw counter value, call the <a href="https://msdn.microsoft.com/bb246c82-8748-4e2f-9f44-a206199aff90">PdhGetRawCounterValue</a> function. If you want to compute a displayable value for the counter value, call the <a href="https://msdn.microsoft.com/cd104b26-1498-4f95-a411-97d868b43836">PdhGetFormattedCounterValue</a>. If the counter path contains a wildcard for the instance name, instead call the <a href="https://msdn.microsoft.com/03b30d08-6901-45cd-bd6d-d2672eb0f914">PdhGetRawCounterArray</a> and <a href="https://msdn.microsoft.com/0f388c7e-d0c8-461d-908c-48af92166996">PdhGetFormattedCounterArray</a> functions, respectively.

When 
<a href="https://msdn.microsoft.com/3fa1d193-03d0-44d8-a32b-b7754594d0ca">PdhCollectQueryDataEx</a> is called for data from one counter instance only, and the counter instance does not exist, the function returns PDH_NO_DATA. However, if data from more than one counter is queried, 
<b>PdhCollectQueryDataEx</b> may return ERROR_SUCCESS even if one of the counter instances does not yet exist. This is because it is not known if the specified counter instance does not exist, or if it will exist but has not yet been created. In this case, call 
the <a href="https://msdn.microsoft.com/bb246c82-8748-4e2f-9f44-a206199aff90">PdhGetRawCounterValue</a> or 
<a href="https://msdn.microsoft.com/cd104b26-1498-4f95-a411-97d868b43836">PdhGetFormattedCounterValue</a> function for each of the counter instances of interest to determine whether they exist.




## -see-also




<a href="https://msdn.microsoft.com/1d83325b-8deb-4731-9df4-6201da292cdc">PdhCollectQueryData</a>



<a href="https://msdn.microsoft.com/cd104b26-1498-4f95-a411-97d868b43836">PdhGetFormattedCounterValue</a>



<a href="https://msdn.microsoft.com/bb246c82-8748-4e2f-9f44-a206199aff90">PdhGetRawCounterValue</a>



<a href="https://msdn.microsoft.com/ec4e5353-c7f5-4957-b7f4-39df508846a0">PdhOpenQuery</a>
 

 

