---
UID: NF:control.IMediaEvent.GetEvent
title: IMediaEvent::GetEvent
author: windows-sdk-content
description: The GetEvent method retrieves the next event notification from the event queue.
old-location: dshow\imediaevent_getevent.htm
tech.root: DirectShow
ms.assetid: d7cbbf6d-c741-416f-b8dd-d9ca012d309a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetEvent, GetEvent method [DirectShow], GetEvent method [DirectShow],IMediaEvent interface, GetEvent method [DirectShow],IMediaEventEx interface, IMediaEvent interface [DirectShow],GetEvent method, IMediaEvent.GetEvent, IMediaEvent::GetEvent, IMediaEventEx interface [DirectShow],GetEvent method, IMediaEventEx::GetEvent, IMediaEventGetEvent, control/IMediaEvent::GetEvent, control/IMediaEventEx::GetEvent, dshow.imediaevent_getevent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: control.h
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
 - IMediaEvent.GetEvent
 - IMediaEventEx.GetEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaEvent::GetEvent


## -description



The <code>GetEvent</code> method retrieves the next event notification from the event queue.




## -parameters




### -param lEventCode [out]

Pointer to a variable that receives the event code.


### -param lParam1 [out]

Pointer to a variable that receives the first event parameter.


### -param lParam2 [out]

Pointer to a variable that receives the second event parameter.


### -param msTimeout [in]

Time-out interval, in milliseconds. Use INFINITE to block until there is an event.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

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
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
Timeout expired.

</td>
</tr>
</table>
 




## -remarks



If no event is on the queue, this method waits up to <i>msTimeout</i> milliseconds for an event to arrive. Avoid using a time-out interval of INFINITE, because threads cannot process any messages while waiting in <code>GetEvent</code>. If you call <code>GetEvent</code> from the same thread that processes Windows messages, specify only small wait times, in order to remain responsive to user input.

After calling <code>GetEvent</code>, call the <a href="https://msdn.microsoft.com/en-us/library/Dd406905(v=VS.85).aspx">IMediaEvent::FreeEventParams</a> method to release any resources allocated for the event parameters.

For a list of notification codes and event parameter values, see <a href="https://msdn.microsoft.com/en-us/library/Dd375625(v=VS.85).aspx">Event Notification Codes</a>.

Because this method removes the event from the filter graph event queue, there is no way for multiple clients to monitor events from the same graph.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd406896(v=VS.85).aspx">IMediaEvent Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd406897(v=VS.85).aspx">IMediaEventEx</a>
 

 

