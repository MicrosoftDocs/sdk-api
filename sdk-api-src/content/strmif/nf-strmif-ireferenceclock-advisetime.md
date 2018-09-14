---
UID: NF:strmif.IReferenceClock.AdviseTime
title: IReferenceClock::AdviseTime
author: windows-sdk-content
description: The AdviseTime method creates a one-shot advise request.
old-location: dshow\ireferenceclock_advisetime.htm
tech.root: DirectShow
ms.assetid: 22f0c987-a3ae-4d6e-9184-a0a4282340aa
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: AdviseTime, AdviseTime method [DirectShow], AdviseTime method [DirectShow],IReferenceClock interface, IReferenceClock interface [DirectShow],AdviseTime method, IReferenceClock.AdviseTime, IReferenceClock::AdviseTime, IReferenceClockAdviseTime, dshow.ireferenceclock_advisetime, strmif/IReferenceClock::AdviseTime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IReferenceClock.AdviseTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IReferenceClock::AdviseTime


## -description



The <code>AdviseTime</code> method creates a one-shot advise request.




## -parameters




### -param baseTime

TBD


### -param streamTime

TBD


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
 

 

