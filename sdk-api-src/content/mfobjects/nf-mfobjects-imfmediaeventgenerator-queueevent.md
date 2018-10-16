---
UID: NF:mfobjects.IMFMediaEventGenerator.QueueEvent
title: IMFMediaEventGenerator::QueueEvent
author: windows-sdk-content
description: Puts a new event in the object's queue.
old-location: mf\imfmediaeventgenerator_queueevent.htm
tech.root: medfound
ms.assetid: 3bc33665-1385-41e1-9ad0-991fc93e91c0
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: 3bc33665-1385-41e1-9ad0-991fc93e91c0, IMFMediaEventGenerator interface [Media Foundation],QueueEvent method, IMFMediaEventGenerator.QueueEvent, IMFMediaEventGenerator::QueueEvent, QueueEvent, QueueEvent method [Media Foundation], QueueEvent method [Media Foundation],IMFMediaEventGenerator interface, mf.imfmediaeventgenerator_queueevent, mfobjects/IMFMediaEventGenerator::QueueEvent
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
 - IMFMediaEventGenerator.QueueEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEventGenerator::QueueEvent


## -description



Puts a new event in the object's queue.




## -parameters




### -param met [in]

Specifies the event type. The event type is returned by the event's <a href="https://msdn.microsoft.com/b62e0d9f-dada-4b75-a8d3-568ee2955888">IMFMediaEvent::GetType</a> method. For a list of event types, see <a href="https://msdn.microsoft.com/d925f63d-3359-4ba1-802f-0c2b11a3f973">Media Foundation Events</a>.


### -param guidExtendedType [in]

The extended type. If the event does not have an extended type, use the value GUID_NULL. The extended type is returned by the event's <a href="https://msdn.microsoft.com/56284491-6f84-467e-9fac-46b04db4024a">IMFMediaEvent::GetExtendedType</a> method.


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
The object was shut down.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a37d0840-c896-43a0-b3d1-c2a6aaff1b25">IMFMediaEventGenerator</a>



<a href="https://msdn.microsoft.com/2e003ad4-9fcb-4834-a335-e4969ffd3a00">Media Event Generators</a>
 

 

