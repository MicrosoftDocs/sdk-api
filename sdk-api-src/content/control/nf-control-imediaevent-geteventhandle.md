---
UID: NF:control.IMediaEvent.GetEventHandle
title: IMediaEvent::GetEventHandle
author: windows-sdk-content
description: The GetEventHandle method retrieves a handle to a manual-reset event that remains signaled while the queue contains event notifications.
old-location: dshow\imediaevent_geteventhandle.htm
tech.root: DirectShow
ms.assetid: 83db8d24-d872-4a90-a896-1cc51273b551
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetEventHandle, GetEventHandle method [DirectShow], GetEventHandle method [DirectShow],IMediaEvent interface, IMediaEvent interface [DirectShow],GetEventHandle method, IMediaEvent.GetEventHandle, IMediaEvent::GetEventHandle, IMediaEventGetEventHandle, control/IMediaEvent::GetEventHandle, dshow.imediaevent_geteventhandle
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
 - IMediaEvent.GetEventHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaEvent::GetEventHandle


## -description



The <code>GetEventHandle</code> method retrieves a handle to a manual-reset event that remains signaled while the queue contains event notifications.




## -parameters




### -param hEvent [out]

Pointer to a variable that receives the event handle.


## -returns



Returns S_OK.




## -remarks



The Filter Graph Manager keeps a manual-reset event that reflects the state of the event queue. If the queue contains event notifications, the manual-reset event is signaled. If the queue is empty, the <a href="https://msdn.microsoft.com/d7cbbf6d-c741-416f-b8dd-d9ca012d309a">IMediaEvent::GetEvent</a> method resets the event.

An application can use this event to determine the state of the queue. First call <code>GetEventHandle</code> to obtain a handle to the event. Wait for the event to be signaled, using a function such as <a href="https://msdn.microsoft.com/e37ebff7-b44e-469d-81ab-7a6bd1a0c822">WaitForSingleObject</a>. When the event is signaled, call the <a href="https://msdn.microsoft.com/d7cbbf6d-c741-416f-b8dd-d9ca012d309a">IMediaEvent::GetEvent</a> method to retrieve the next event notification from the queue. The Filter Graph Manager keeps the event signaled until the queue is empty; then it resets the event.

Do not close the event handle returned by this method, because the event handle is used internally by the filter graph. Also, do not use the handle after you release the Filter Graph Manager, because the handle becomes invalid after the Filter Graph Manager is destroyed. (To avoid this error, it is a good idea to duplicate the handle by calling <a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a>, and use the duplicate instead of the original handle. Close the duplicate handle when you are finished.)

For Automation compatibility, this method takes a pointer to an <a href="https://msdn.microsoft.com/2c260592-98a9-4f85-accf-282bd5231d5c">OAEVENT</a> type. In C++, declare a variable of type <b>HANDLE</b> and cast it an <b>OAEVENT</b> pointer, as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HANDLE hEvent;
GetEventHandle( (OAEVENT*) &amp;hEvent );
</pre>
</td>
</tr>
</table></span></div>
Another way for applications to monitor the event queue is by calling the <a href="https://msdn.microsoft.com/3e582c79-b8c7-40be-97fd-75d5b7965570">IMediaEventEx::SetNotifyWindow</a> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/651561d1-4e7e-48de-9cba-769ddb553e63">IMediaEvent Interface</a>
 

 

