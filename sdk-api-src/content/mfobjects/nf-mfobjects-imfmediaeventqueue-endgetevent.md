---
UID: NF:mfobjects.IMFMediaEventQueue.EndGetEvent
title: IMFMediaEventQueue::EndGetEvent
author: windows-sdk-content
description: Completes an asynchronous request for the next event in the queue.Call this method inside your implementation of IMFMediaEventGenerator::EndGetEvent. Pass the parameters from that method directly to this method.
old-location: mf\imfmediaeventqueue_endgetevent.htm
tech.root: medfound
ms.assetid: bb0ea226-9dc0-43e3-a482-cfec531b5734
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: EndGetEvent, EndGetEvent method [Media Foundation], EndGetEvent method [Media Foundation],IMFMediaEventQueue interface, IMFMediaEventQueue interface [Media Foundation],EndGetEvent method, IMFMediaEventQueue.EndGetEvent, IMFMediaEventQueue::EndGetEvent, bb0ea226-9dc0-43e3-a482-cfec531b5734, mf.imfmediaeventqueue_endgetevent, mfobjects/IMFMediaEventQueue::EndGetEvent
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
 - IMFMediaEventQueue.EndGetEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfobjects.h
: 
- IMFMediaEventQueue.EndGetEvent
: 
---

# IMFMediaEventQueue::EndGetEvent


## -description



Completes an asynchronous request for the next event in the queue.

Call this method inside your implementation of <a href="https://msdn.microsoft.com/6b38e984-d818-4f69-af28-8b54153faebb">IMFMediaEventGenerator::EndGetEvent</a>. Pass the parameters from that method directly to this method.




## -parameters




### -param pResult [in]

Pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface.


### -param ppEvent [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/b4f686be-9472-433c-b983-6c48dfd3ac76">IMFMediaEvent</a> interface of the event object. The caller must release the interface.


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
 

 

