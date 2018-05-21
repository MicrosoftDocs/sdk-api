---
UID: NN:mfobjects.IMFMediaEventQueue
title: IMFMediaEventQueue
author: windows-driver-content
description: Provides an event queue for applications that need to implement the IMFMediaEventGenerator interface.
old-location: mf\imfmediaeventqueue.htm
old-project: medfound
ms.assetid: e1698caa-db70-436d-af6a-64c6e7247590
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: IMFMediaEventQueue, IMFMediaEventQueue interface [Media Foundation], IMFMediaEventQueue interface [Media Foundation],described, e1698caa-db70-436d-af6a-64c6e7247590, mf.imfmediaeventqueue, mfobjects/IMFMediaEventQueue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_FILE_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFMediaEventQueue
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEventQueue interface


## -description


Provides an event queue for applications that need to implement the <a href="https://msdn.microsoft.com/a37d0840-c896-43a0-b3d1-c2a6aaff1b25">IMFMediaEventGenerator</a> interface.

This interface is exposed by a helper object that implements an event queue. If you are writing a component that implements the <a href="https://msdn.microsoft.com/a37d0840-c896-43a0-b3d1-c2a6aaff1b25">IMFMediaEventGenerator</a> interface, you can use this object in your implementation. The event queue object is thread safe and provides methods to queue events and to pull them from the queue either synchronously or asynchronously. To create the event queue object, call <a href="https://msdn.microsoft.com/214cea99-37cf-4571-aa00-7b3e220a6b84">MFCreateEventQueue</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEventQueue</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaEventQueue</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/454d4b3b-6251-4b7e-b8f3-ff7cff5269b5">BeginGetEvent</a>
</td>
<td align="left" width="63%">
Begins an asynchronous request for the next event in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb0ea226-9dc0-43e3-a482-cfec531b5734">EndGetEvent</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request for the next event in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7c48607-f410-47ee-8cc6-38123919da55">GetEvent</a>
</td>
<td align="left" width="63%">
Retrieves the next event in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb04ce9f-fb64-438f-ad4d-ba1fb849d59c">QueueEvent</a>
</td>
<td align="left" width="63%">
Puts an event in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e51653a4-8f71-44f3-90e8-2052db521307">QueueEventParamUnk</a>
</td>
<td align="left" width="63%">
Creates an event, sets an <b>IUnknown</b> pointer as the event data, and puts the event in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2bafeca-76e7-4df4-94a7-86aef04f3a35">QueueEventParamVar</a>
</td>
<td align="left" width="63%">
Creates an event, sets a <b>PROPVARIANT</b> as the event data, and puts the event in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a>
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




<a href="https://msdn.microsoft.com/2e003ad4-9fcb-4834-a335-e4969ffd3a00">Media Event Generators</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

