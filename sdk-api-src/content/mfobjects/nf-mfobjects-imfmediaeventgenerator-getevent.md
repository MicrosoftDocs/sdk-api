---
UID: NF:mfobjects.IMFMediaEventGenerator.GetEvent
title: IMFMediaEventGenerator::GetEvent
author: windows-sdk-content
description: Retrieves the next event in the queue. This method is synchronous.
old-location: mf\imfmediaeventgenerator_getevent.htm
old-project: medfound
ms.assetid: e78464b5-ec6b-4739-a135-352fa297916a
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 0, GetEvent, GetEvent method [Media Foundation], GetEvent method [Media Foundation],IMFMediaEventGenerator interface, IMFMediaEventGenerator interface [Media Foundation],GetEvent method, IMFMediaEventGenerator.GetEvent, IMFMediaEventGenerator::GetEvent, MF_EVENT_FLAG_NO_WAIT, e78464b5-ec6b-4739-a135-352fa297916a, mf.imfmediaeventgenerator_getevent, mfobjects/IMFMediaEventGenerator::GetEvent
ms.prod: windows
ms.technology: windows-sdk
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
 - IMFMediaEventGenerator.GetEvent
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEventGenerator::GetEvent


## -description



Retrieves the next event in the queue. This method is synchronous.




## -parameters




### -param dwFlags [in]

Specifies one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
The method blocks until the event generator queues an event.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_EVENT_FLAG_NO_WAIT"></a><a id="mf_event_flag_no_wait"></a><dl>
<dt><b>MF_EVENT_FLAG_NO_WAIT</b></dt>
</dl>
</td>
<td width="60%">
The method returns immediately.

</td>
</tr>
</table>
 


### -param ppEvent [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/b4f686be-9472-433c-b983-6c48dfd3ac76">IMFMediaEvent</a> interface. The caller must release the interface.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_MULTIPLE_SUBSCRIBERS</b></dt>
</dl>
</td>
<td width="60%">
There is a pending request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NO_EVENTS_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
There are no events in the queue.

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
 




## -remarks



This method executes synchronously.

If the queue already contains an event, the method returns S_OK immediately. If the queue does not contain an event, the behavior depends on the value of <i>dwFlags</i>:

<ul>
<li>
If <i>dwFlags</i> is 0, the method blocks indefinitely until a new event is queued, or until the event generator is shut down.

</li>
<li>
If <i>dwFlags</i> is MF_EVENT_FLAG_NO_WAIT, the method fails immediately with the return code MF_E_NO_EVENTS_AVAILABLE.

</li>
</ul>
This method returns MF_E_MULTIPLE_SUBSCRIBERS if you previously called <a href="https://msdn.microsoft.com/a2afddac-46e9-4928-8b5b-44f3fc7c33d3">IMFMediaEventGenerator::BeginGetEvent</a> and have not yet called <a href="https://msdn.microsoft.com/6b38e984-d818-4f69-af28-8b54153faebb">IMFMediaEventGenerator::EndGetEvent</a>.




## -see-also




<a href="https://msdn.microsoft.com/a37d0840-c896-43a0-b3d1-c2a6aaff1b25">IMFMediaEventGenerator</a>



<a href="https://msdn.microsoft.com/2e003ad4-9fcb-4834-a335-e4969ffd3a00">Media Event Generators</a>
 

 

