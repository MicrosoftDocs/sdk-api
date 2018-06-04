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

# IMFTimer::SetTimer


## -description



Sets a timer that invokes a callback at the specified time.




## -parameters




### -param dwFlags [in]

Bitwise OR of zero or more flags from the <a href="https://msdn.microsoft.com/bd94247a-ed58-4857-a39d-16880eea75e0">MFTIMER_FLAGS</a> enumeration.


### -param llClockTime [in]

The time at which the timer should fire, in units of the clock's frequency. The time is either absolute or relative to the current time, depending on the value of <i>dwFlags</i>.


### -param pCallback [in]

Pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface. The callback's <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">Invoke</a> method is called at the time specified in the <i>llClockTime</i> parameter.


### -param punkState [in]

Pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.


### -param ppunkKey [out]

Receives a pointer to the <b>IUnknown</b> interface of a cancellation object. The caller must release the interface. To cancel the timer, pass this pointer to the <a href="https://msdn.microsoft.com/3fa65809-1652-4903-92ad-1034bcdf0743">IMFTimer::CancelTimer</a> method. This parameter can be <b>NULL</b>.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The clock was shut down.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_S_CLOCK_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded, but the clock is stopped.

</td>
</tr>
</table>
 




## -remarks



If the clock is stopped, the method returns MF_S_CLOCK_STOPPED. The callback will not be invoked until the clock is started.




## -see-also




<a href="https://msdn.microsoft.com/152594df-de3d-4f6f-9277-dba95ab3533a">IMFTimer</a>
 

 

