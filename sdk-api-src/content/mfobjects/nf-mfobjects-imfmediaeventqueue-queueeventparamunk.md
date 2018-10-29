---
UID: NF:mfobjects.IMFMediaEventQueue.QueueEventParamUnk
title: IMFMediaEventQueue::QueueEventParamUnk
author: windows-sdk-content
description: Creates an event, sets an IUnknown pointer as the event data, and puts the event in the queue.
old-location: mf\imfmediaeventqueue_queueeventparamunk.htm
tech.root: medfound
ms.assetid: e51653a4-8f71-44f3-90e8-2052db521307
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IMFMediaEventQueue interface [Media Foundation],QueueEventParamUnk method, IMFMediaEventQueue.QueueEventParamUnk, IMFMediaEventQueue::QueueEventParamUnk, QueueEventParamUnk, QueueEventParamUnk method [Media Foundation], QueueEventParamUnk method [Media Foundation],IMFMediaEventQueue interface, e51653a4-8f71-44f3-90e8-2052db521307, mf.imfmediaeventqueue_queueeventparamunk, mfobjects/IMFMediaEventQueue::QueueEventParamUnk
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMFMediaEventQueue.QueueEventParamUnk
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEventQueue::QueueEventParamUnk


## -description



Creates an event, sets an <b>IUnknown</b> pointer as the event data, and puts the event in the queue.




## -parameters




### -param met [in]

Specifies the event type of the event to be added to the queue. The event type is returned by the event's <a href="https://msdn.microsoft.com/b62e0d9f-dada-4b75-a8d3-568ee2955888">IMFMediaEvent::GetType</a> method. For a list of event types, see <a href="https://msdn.microsoft.com/d925f63d-3359-4ba1-802f-0c2b11a3f973">Media Foundation Events</a>.


### -param guidExtendedType [in]

The extended type of the event. If the event does not have an extended type, use the value GUID_NULL. The extended type is returned by the event's <a href="https://msdn.microsoft.com/56284491-6f84-467e-9fac-46b04db4024a">IMFMediaEvent::GetExtendedType</a> method.


### -param hrStatus [in]

A success or failure code indicating the status of the event. This value is returned by the event's <a href="https://msdn.microsoft.com/e2fc6c81-11c0-4947-b647-3e74a73ee5a2">IMFMediaEvent::GetStatus</a> method.


### -param pUnk [in]

Pointer to the <b>IUnknown</b> interface. The method sets this pointer as the event value. The pointer is returned by the event's <a href="https://msdn.microsoft.com/05e57b40-2565-4312-866e-50f0c7d62c4a">IMFMediaEvent::GetValue</a> method.


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



Call this method when your component needs to raise an event that contains an <b>IUnknown</b> pointer value and no attributes. If the event contains attributes, use <a href="https://msdn.microsoft.com/eb04ce9f-fb64-438f-ad4d-ba1fb849d59c">IMFMediaEventQueue::QueueEvent</a> instead.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/e1698caa-db70-436d-af6a-64c6e7247590">IMFMediaEventQueue</a>
 

 

