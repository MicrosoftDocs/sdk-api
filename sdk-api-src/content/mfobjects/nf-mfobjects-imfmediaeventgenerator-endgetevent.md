---
UID: NF:mfobjects.IMFMediaEventGenerator.EndGetEvent
title: IMFMediaEventGenerator::EndGetEvent (mfobjects.h)
author: windows-sdk-content
description: Completes an asynchronous request for the next event in the queue.
old-location: mf\imfmediaeventgenerator_endgetevent.htm
tech.root: medfound
ms.assetid: 6b38e984-d818-4f69-af28-8b54153faebb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 6b38e984-d818-4f69-af28-8b54153faebb, EndGetEvent, EndGetEvent method [Media Foundation], EndGetEvent method [Media Foundation],IMFMediaEventGenerator interface, IMFMediaEventGenerator interface [Media Foundation],EndGetEvent method, IMFMediaEventGenerator.EndGetEvent, IMFMediaEventGenerator::EndGetEvent, mf.imfmediaeventgenerator_endgetevent, mfobjects/IMFMediaEventGenerator::EndGetEvent
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
 - IMFMediaEventGenerator.EndGetEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEventGenerator::EndGetEvent


## -description



Completes an asynchronous request for the next event in the queue.




## -parameters




### -param pResult [in]

Pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">Invoke</a> method.


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
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The object was shut down.

</td>
</tr>
</table>
 




## -remarks



Call this method from inside your application's <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method. For example code, see <a href="https://msdn.microsoft.com/a2afddac-46e9-4928-8b5b-44f3fc7c33d3">IMFMediaEventGenerator::BeginGetEvent</a>.




## -see-also




<a href="https://msdn.microsoft.com/a37d0840-c896-43a0-b3d1-c2a6aaff1b25">IMFMediaEventGenerator</a>



<a href="https://msdn.microsoft.com/2e003ad4-9fcb-4834-a335-e4969ffd3a00">Media Event Generators</a>
 

 

