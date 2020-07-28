---
UID: NF:control.IMediaEvent.GetEventHandle
title: IMediaEvent::GetEventHandle (control.h)
description: The GetEventHandle method retrieves a handle to a manual-reset event that remains signaled while the queue contains event notifications.
helpviewer_keywords: ["GetEventHandle","GetEventHandle method [DirectShow]","GetEventHandle method [DirectShow]","IMediaEvent interface","IMediaEvent interface [DirectShow]","GetEventHandle method","IMediaEvent.GetEventHandle","IMediaEvent::GetEventHandle","IMediaEventGetEventHandle","control/IMediaEvent::GetEventHandle","dshow.imediaevent_geteventhandle"]
old-location: dshow\imediaevent_geteventhandle.htm
tech.root: dshow
ms.assetid: 83db8d24-d872-4a90-a896-1cc51273b551
ms.date: 12/05/2018
ms.keywords: GetEventHandle, GetEventHandle method [DirectShow], GetEventHandle method [DirectShow],IMediaEvent interface, IMediaEvent interface [DirectShow],GetEventHandle method, IMediaEvent.GetEventHandle, IMediaEvent::GetEventHandle, IMediaEventGetEventHandle, control/IMediaEvent::GetEventHandle, dshow.imediaevent_geteventhandle
f1_keywords:
- control/IMediaEvent.GetEventHandle
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



The Filter Graph Manager keeps a manual-reset event that reflects the state of the event queue. If the queue contains event notifications, the manual-reset event is signaled. If the queue is empty, the <a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-imediaevent-getevent">IMediaEvent::GetEvent</a> method resets the event.

An application can use this event to determine the state of the queue. First call <code>GetEventHandle</code> to obtain a handle to the event. Wait for the event to be signaled, using a function such as <a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>. When the event is signaled, call the <a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-imediaevent-getevent">IMediaEvent::GetEvent</a> method to retrieve the next event notification from the queue. The Filter Graph Manager keeps the event signaled until the queue is empty; then it resets the event.

Do not close the event handle returned by this method, because the event handle is used internally by the filter graph. Also, do not use the handle after you release the Filter Graph Manager, because the handle becomes invalid after the Filter Graph Manager is destroyed. (To avoid this error, it is a good idea to duplicate the handle by calling <a href="https://docs.microsoft.com/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a>, and use the duplicate instead of the original handle. Close the duplicate handle when you are finished.)

For Automation compatibility, this method takes a pointer to an <a href="https://docs.microsoft.com/windows/desktop/DirectShow/oaevent">OAEVENT</a> type. In C++, declare a variable of type <b>HANDLE</b> and cast it an <b>OAEVENT</b> pointer, as follows:


```cpp

HANDLE hEvent;
GetEventHandle( (OAEVENT*) &hEvent );

```


Another way for applications to monitor the event queue is by calling the <a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-imediaeventex-setnotifywindow">IMediaEventEx::SetNotifyWindow</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-imediaevent">IMediaEvent Interface</a>
 

 

