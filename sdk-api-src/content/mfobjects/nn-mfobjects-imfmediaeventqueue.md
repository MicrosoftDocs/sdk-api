---
UID: NN:mfobjects.IMFMediaEventQueue
title: IMFMediaEventQueue (mfobjects.h)

description: Provides an event queue for applications that need to implement the IMFMediaEventGenerator interface.
old-location: mf\imfmediaeventqueue.htm
tech.root: medfound
ms.assetid: e1698caa-db70-436d-af6a-64c6e7247590

ms.date: 12/05/2018
ms.keywords: IMFMediaEventQueue, IMFMediaEventQueue interface [Media Foundation], IMFMediaEventQueue interface [Media Foundation],described, e1698caa-db70-436d-af6a-64c6e7247590, mf.imfmediaeventqueue, mfobjects/IMFMediaEventQueue
ms.topic: interface
f1_keywords: 
 - "mfobjects/IMFMediaEventQueue"
dev_langs:
 - c++
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaEventQueue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEventQueue interface


## -description


Provides an event queue for applications that need to implement the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a> interface.

This interface is exposed by a helper object that implements an event queue. If you are writing a component that implements the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a> interface, you can use this object in your implementation. The event queue object is thread safe and provides methods to queue events and to pull them from the queue either synchronously or asynchronously. To create the event queue object, call <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue">MFCreateEventQueue</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEventQueue</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaEventQueue</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEventQueue</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent">BeginGetEvent</a>
</td>
<td align="left" width="63%">
Begins an asynchronous request for the next event in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-endgetevent">EndGetEvent</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request for the next event in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-getevent">GetEvent</a>
</td>
<td align="left" width="63%">
Retrieves the next event in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent">QueueEvent</a>
</td>
<td align="left" width="63%">
Puts an event in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamunk">QueueEventParamUnk</a>
</td>
<td align="left" width="63%">
Creates an event, sets an <b>IUnknown</b> pointer as the event data, and puts the event in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamvar">QueueEventParamVar</a>
</td>
<td align="left" width="63%">
Creates an event, sets a <b>PROPVARIANT</b> as the event data, and puts the event in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown">Shutdown</a>
</td>
<td align="left" width="63%">
Shuts down the event queue.

</td>
</tr>
</table> 


## -remarks



This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-event-generators">Media Event Generators</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

