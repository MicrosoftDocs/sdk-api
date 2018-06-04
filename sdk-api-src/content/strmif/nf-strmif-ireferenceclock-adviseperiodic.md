---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IReferenceClock::AdvisePeriodic


## -description



The <code>AdvisePeriodic</code> method creates a periodic advise request.




## -parameters




### -param startTime




### -param periodTime




### -param hSemaphore [in]

Handle to a semaphore, created by the caller.


### -param pdwAdviseCookie [out]

Pointer to a variable that receives an identifier for the advise request.


#### - rtPeriodTime [in]

Time between notifications, in 100-nanosecond units. Must be greater than zero.


#### - rtStartTime [in]

Time of the first notification, in 100-nanosecond units. Must be greater than zero and less than MAX_TIME.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid time values.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>
 




## -remarks



At each notification time, the clock releases the semaphore specified in the <i>hSemaphore</i> parameter. When no further notifications are required, call <a href="https://msdn.microsoft.com/1f032036-4502-473a-93e1-976a66d8bde1">IReferenceClock::Unadvise</a> and pass the <i>pdwAdviseToken</i> value returned from this call.

The following code example creates an advise request that signals five seconds from the time it is created, and again every second thereafter:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
IReferenceClock *pRefClock = NULL;
// Get an IReferenceClock pointer (not shown).

DWORD          dwAdviseToken;
HANDLE         hSemaphore = CreateSemaphore(NULL, 0, 0x7FFFFFFF, NULL);
REFERENCE_TIME rtPeriodTime = 10000000; // A one-second interval
REFERENCE_TIME rtNow;

pRefClock-&gt;GetTime(&amp;rtNow);
pRefClock-&gt;AdvisePeriodic(rtNow + (5 * rtPeriodTime),
                          rtPeriodTime, 
                          hSemaphore, 
                          &amp;dwAdviseToken);
...

pRefClock-&gt;Unadvise(dwAdviseToken);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9818c67d-dfbe-4498-a744-d2efaa4bfb58">IReferenceClock Interface</a>
 

 

