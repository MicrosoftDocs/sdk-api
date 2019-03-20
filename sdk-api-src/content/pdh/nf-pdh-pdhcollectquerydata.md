---
UID: NF:pdh.PdhCollectQueryData
title: PdhCollectQueryData function (pdh.h)
author: windows-sdk-content
description: Collects the current raw data value for all counters in the specified query and updates the status code of each counter.
old-location: perf\pdhcollectquerydata.htm
tech.root: perfctrs
ms.assetid: 1d83325b-8deb-4731-9df4-6201da292cdc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PdhCollectQueryData, PdhCollectQueryData function [Perf], _win32_pdhcollectquerydata, base.pdhcollectquerydata, pdh/PdhCollectQueryData, perf.pdhcollectquerydata
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
 - PdhCollectQueryData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PdhCollectQueryData function


## -description


Collects the current raw data value for all counters in the specified query and updates the status code of each counter.
		


## -parameters




### -param hQuery [in, out]

Handle of the query for which you want to collect data. The <a href="https://msdn.microsoft.com/ec4e5353-c7f5-4957-b7f4-39df508846a0">PdhOpenQuery</a> function returns this handle.


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
The query does not currently contain any counters. The query may not contain data because the user is not running with an elevated token (see <a href="https://msdn.microsoft.com/85c5f38f-d8d7-4203-adc0-4869d6078351">Limited User Access Support</a>).

</td>
</tr>
</table>
 




## -remarks



Call this function when you want to collect counter data for the counters in the query. PDH stores the raw counter values for the current and previous collection. 

If you want to retrieve the current raw counter value, call the <a href="https://msdn.microsoft.com/bb246c82-8748-4e2f-9f44-a206199aff90">PdhGetRawCounterValue</a> function. If you want to compute a displayable value for the counter value, call the <a href="https://msdn.microsoft.com/cd104b26-1498-4f95-a411-97d868b43836">PdhGetFormattedCounterValue</a> function. If the counter path contains a wildcard for the instance name, instead call the <a href="https://msdn.microsoft.com/03b30d08-6901-45cd-bd6d-d2672eb0f914">PdhGetRawCounterArray</a> and <a href="https://msdn.microsoft.com/0f388c7e-d0c8-461d-908c-48af92166996">PdhGetFormattedCounterArray</a> functions, respectively.

When 
<b>PdhCollectQueryData</b> is called for data from one counter instance only and the counter instance does not exist, the function returns PDH_NO_DATA. However, if data from more than one counter is queried, 
<b>PdhCollectQueryData</b> may return ERROR_SUCCESS even if one of the counter instances does not yet exist. This is because it is not known if the specified counter instance does not exist, or if it will exist but has not yet been created. In this case, call 
<a href="https://msdn.microsoft.com/bb246c82-8748-4e2f-9f44-a206199aff90">PdhGetRawCounterValue</a> or 
<a href="https://msdn.microsoft.com/cd104b26-1498-4f95-a411-97d868b43836">PdhGetFormattedCounterValue</a> for each of the counter instances of interest to determine whether they exist.

The following shows the syntax if calling this function from Visual Basic.

<pre class="syntax" xml:space="preserve"><code>PdhCollectQueryData(
  ByVal QueryHandle as Long  
)
as Long</code></pre>



#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/44c5cfa8-6449-45d8-ac30-979b99c086de">Browsing Performance Counters</a> or 
<a href="https://msdn.microsoft.com/acec1506-473a-43c9-9b57-ad8c00e8f250">Reading Performance Data from a Log File</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/cd104b26-1498-4f95-a411-97d868b43836">PdhGetFormattedCounterValue</a>



<a href="https://msdn.microsoft.com/bb246c82-8748-4e2f-9f44-a206199aff90">PdhGetRawCounterValue</a>
 

 

