---
UID: NN:control.IMediaEvent
title: IMediaEvent
author: windows-driver-content
description: The IMediaEvent interface contains methods for retrieving event notifications and for overriding the Filter Graph Manager's default handling of events.
old-location: dshow\imediaevent.htm
old-project: DirectShow
ms.assetid: 651561d1-4e7e-48de-9cba-769ddb553e63
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IMediaEvent, IMediaEvent interface [DirectShow], IMediaEvent interface [DirectShow], described, IMediaEventInterface, control/IMediaEvent, dshow.imediaevent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: WMPContextMenuInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IMediaEvent
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IMediaEvent interface


## -description



The <code>IMediaEvent</code> interface contains methods for retrieving event notifications and for overriding the Filter Graph Manager's default handling of events. The <a href="https://msdn.microsoft.com/9d367b0a-c7ec-49d4-a41e-045ac81d2c51">IMediaEventEx</a> interface inherits this interface and extends it.

The Filter Graph Manager implements this interface. Applications can use it to respond to events that occur in the filter graph, such as the end of a stream or a rendering error. Filters post events to the filter graph using the <a href="https://msdn.microsoft.com/50aa04b4-9a04-4d0d-a558-42595a69aef7">IMediaEventSink</a> interface.

For more information about event notification, see <a href="https://msdn.microsoft.com/301116a5-24e3-4c6d-8c80-bec77c7d62d7">Event Notification in DirectShow</a>. For a list of system-defined event notifications, see <a href="https://msdn.microsoft.com/339ffcd9-7724-4c92-b241-afbed81d9380">Event Notification Codes</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaEvent</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IMediaEvent</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/955d0494-8418-42a1-ab6e-2c779165f578">CancelDefaultHandling</a>
</td>
<td align="left" width="63%">
Cancels the Filter Graph Manager's default handling for a specified event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d98f37a4-3482-4cf7-bede-c7e7be70652a">FreeEventParams</a>
</td>
<td align="left" width="63%">
Frees resources associated with the parameters of an event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7cbbf6d-c741-416f-b8dd-d9ca012d309a">GetEvent</a>
</td>
<td align="left" width="63%">
Retrieves the next event notification from the event queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83db8d24-d872-4a90-a896-1cc51273b551">GetEventHandle</a>
</td>
<td align="left" width="63%">
Retrieves a handle to a manual-reset event that remains signaled while the queue contains event notifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2df616b0-b944-44ab-8147-4f70796dd2a2">RestoreDefaultHandling</a>
</td>
<td align="left" width="63%">
Restores the Filter Graph Manager's default handling for a specified event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/760a90fe-7cbc-4f09-ba64-afe0ab0b4c74">WaitForCompletion</a>
</td>
<td align="left" width="63%">
Waits for the filter graph to render all available data.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

