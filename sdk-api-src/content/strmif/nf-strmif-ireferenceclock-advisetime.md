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

# IReferenceClock::AdviseTime


## -description



The <code>AdviseTime</code> method creates a one-shot advise request.




## -parameters




### -param baseTime




### -param streamTime




### -param hEvent [in]

Handle to an event, created by the caller.


### -param pdwAdviseCookie [out]

Pointer to a variable that receives an identifier for the advise request.


#### - rtBaseTime [in]

Base reference time, in 100-nanosecond units. See Remarks.


#### - rtStreamTime [in]

Stream offset time, in 100-nanosecond units. See Remarks.


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



This method creates a one-shot advise request for the reference time <i>rtBaseTime</i> + <i>rtStreamTime</i>. The sum must be greater than zero and less than MAX_TIME, or the method returns E_INVALIDARG. At the requested time, the clock signals the event specified in the <i>hEvent</i> parameter.

To cancel the notification before the time is reached, call the <a href="https://msdn.microsoft.com/1f032036-4502-473a-93e1-976a66d8bde1">Unadvise</a> method and pass the <i>pdwAdviseToken</i> value returned from this call. After the notification has occurred, the clock automatically clears it, so it is not necessary to call <b>Unadvise</b>. However, it is not an error to do so.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9818c67d-dfbe-4498-a744-d2efaa4bfb58">IReferenceClock Interface</a>
 

 

