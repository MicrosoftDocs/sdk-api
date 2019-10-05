---
UID: NN:control.IMediaEvent
title: IMediaEvent (control.h)
author: windows-sdk-content
description: The IMediaEvent interface contains methods for retrieving event notifications and for overriding the Filter Graph Manager's default handling of events.
old-location: dshow\imediaevent.htm
tech.root: DirectShow
ms.assetid: 651561d1-4e7e-48de-9cba-769ddb553e63
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMediaEvent, IMediaEvent interface [DirectShow], IMediaEvent interface [DirectShow],described, IMediaEventInterface, control/IMediaEvent, dshow.imediaevent
ms.topic: interface
f1_keywords: 
 - "control/IMediaEvent"
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
 - IMediaEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaEvent interface


## -description



The <code>IMediaEvent</code> interface contains methods for retrieving event notifications and for overriding the Filter Graph Manager's default handling of events. The <a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-imediaeventex">IMediaEventEx</a> interface inherits this interface and extends it.

The Filter Graph Manager implements this interface. Applications can use it to respond to events that occur in the filter graph, such as the end of a stream or a rendering error. Filters post events to the filter graph using the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imediaeventsink">IMediaEventSink</a> interface.

For more information about event notification, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/event-notification-in-directshow">Event Notification in DirectShow</a>. For a list of system-defined event notifications, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/event-notification-codes">Event Notification Codes</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaEvent</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMediaEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-imediaevent-canceldefaulthandling">CancelDefaultHandling</a>
</td>
<td align="left" width="63%">
Cancels the Filter Graph Manager's default handling for a specified event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-imediaevent-freeeventparams">FreeEventParams</a>
</td>
<td align="left" width="63%">
Frees resources associated with the parameters of an event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-imediaevent-getevent">GetEvent</a>
</td>
<td align="left" width="63%">
Retrieves the next event notification from the event queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-imediaevent-geteventhandle">GetEventHandle</a>
</td>
<td align="left" width="63%">
Retrieves a handle to a manual-reset event that remains signaled while the queue contains event notifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-imediaevent-restoredefaulthandling">RestoreDefaultHandling</a>
</td>
<td align="left" width="63%">
Restores the Filter Graph Manager's default handling for a specified event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-imediaevent-waitforcompletion">WaitForCompletion</a>
</td>
<td align="left" width="63%">
Waits for the filter graph to render all available data.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

