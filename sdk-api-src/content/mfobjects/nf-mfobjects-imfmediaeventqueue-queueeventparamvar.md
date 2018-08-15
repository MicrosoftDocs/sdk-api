---
UID: NF:mfobjects.IMFMediaEventQueue.QueueEventParamVar
title: IMFMediaEventQueue::QueueEventParamVar
author: windows-sdk-content
description: Creates an event, sets a PROPVARIANT as the event data, and puts the event in the queue.Call this method inside your implementation of IMFMediaEventGenerator::QueueEvent.
old-location: mf\imfmediaeventqueue_queueeventparamvar.htm
old-project: medfound
ms.assetid: e2bafeca-76e7-4df4-94a7-86aef04f3a35
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFMediaEventQueue interface [Media Foundation],QueueEventParamVar method, IMFMediaEventQueue.QueueEventParamVar, IMFMediaEventQueue::QueueEventParamVar, QueueEventParamVar, QueueEventParamVar method [Media Foundation], QueueEventParamVar method [Media Foundation],IMFMediaEventQueue interface, e2bafeca-76e7-4df4-94a7-86aef04f3a35, mf.imfmediaeventqueue_queueeventparamvar, mfobjects/IMFMediaEventQueue::QueueEventParamVar
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.redist: 
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
tech.root: 
req.typenames: MF_FILE_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaEventQueue.QueueEventParamVar
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEventQueue::QueueEventParamVar


## -description



Creates an event, sets a <b>PROPVARIANT</b> as the event data, and puts the event in the queue.

Call this method inside your implementation of <a href="https://msdn.microsoft.com/3bc33665-1385-41e1-9ad0-991fc93e91c0">IMFMediaEventGenerator::QueueEvent</a>. Pass the parameters from that method directly to this method.

You can also call this method when your component needs to raise an event that does not contain attributes. If the event data is an <b>IUnknown</b> pointer, you can use <a href="https://msdn.microsoft.com/e51653a4-8f71-44f3-90e8-2052db521307">IMFMediaEventQueue::QueueEventParamUnk</a>. If the event contains attributes, use <a href="https://msdn.microsoft.com/eb04ce9f-fb64-438f-ad4d-ba1fb849d59c">IMFMediaEventQueue::QueueEvent</a> instead.




## -parameters




### -param met [in]

Specifies the type of the event to be added to the queue. The event type is returned by the event's <a href="https://msdn.microsoft.com/b62e0d9f-dada-4b75-a8d3-568ee2955888">IMFMediaEvent::GetType</a> method. For a list of event types, see <a href="https://msdn.microsoft.com/d925f63d-3359-4ba1-802f-0c2b11a3f973">Media Foundation Events</a>.


### -param guidExtendedType [in]

The extended type of the event. If the event does not have an extended type, use the value GUID_NULL. The extended type is returned by the event's <a href="https://msdn.microsoft.com/56284491-6f84-467e-9fac-46b04db4024a">IMFMediaEvent::GetExtendedType</a> method.


### -param hrStatus [in]

A success or failure code indicating the status of the event. This value is returned by the event's <a href="https://msdn.microsoft.com/e2fc6c81-11c0-4947-b647-3e74a73ee5a2">IMFMediaEvent::GetStatus</a> method.


### -param pvValue [in]

Pointer to a <b>PROPVARIANT</b> that contains the event value. This parameter can be <b>NULL</b>. This value is returned by the event's <a href="https://msdn.microsoft.com/05e57b40-2565-4312-866e-50f0c7d62c4a">IMFMediaEvent::GetValue</a> method.


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
The <a href="https://msdn.microsoft.com/6ec52973-0d90-463b-b2be-08d5d6fdcc05">Shutdown</a> method was called.

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




<a href="https://msdn.microsoft.com/e1698caa-db70-436d-af6a-64c6e7247590">IMFMediaEventQueue</a>
 

 

