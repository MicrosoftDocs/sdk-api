---
UID: NF:mfidl.IMFTrackedSample.SetAllocator
title: IMFTrackedSample::SetAllocator
author: windows-sdk-content
description: Sets the owner for the sample.
old-location: mf\imftrackedsample_setallocator.htm
tech.root: medfound
ms.assetid: eb9ffeb3-60af-4cef-bbbc-f4be53d48df0
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IMFTrackedSample interface [Media Foundation],SetAllocator method, IMFTrackedSample.SetAllocator, IMFTrackedSample::SetAllocator, SetAllocator, SetAllocator method [Media Foundation], SetAllocator method [Media Foundation],IMFTrackedSample interface, eb9ffeb3-60af-4cef-bbbc-f4be53d48df0, mf.imftrackedsample_setallocator, mfidl/IMFTrackedSample::SetAllocator
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFTrackedSample.SetAllocator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTrackedSample::SetAllocator


## -description



Sets the owner for the sample.




## -parameters




### -param pSampleAllocator [in]

Pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.


### -param pUnkState [in]

Pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.


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
<dt><b>MF_E_NOTACCEPTING</b></dt>
</dl>
</td>
<td width="60%">
The owner was already set. This method cannot be called twice on the sample.

</td>
</tr>
</table>
 




## -remarks



When this method is called, the sample holds an additional reference count on itself. When every other object releases its reference counts on the sample, the sample invokes the <i>pSampleAllocator</i> callback method. To get a pointer to the sample, call <a href="https://msdn.microsoft.com/b4b871ff-370d-4a37-9fe4-91d1805890eb">IMFAsyncResult::GetObject</a> on the asynchronous result object given to the callback's <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method.

After the callback is invoked, the sample clears the callback. To reinstate the callback, you must call <b>SetAllocator</b> again.

It is safe to pass in the sample's <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> interface pointer as the state object (<i>pUnkState</i>) for the callback. If <i>pUnkState</i> points to the sample, the <b>SetAllocator</b> method accounts for the additional reference count on <i>pUnkState</i>.




## -see-also




<a href="https://msdn.microsoft.com/4ad4b14c-94af-4314-8a16-163579dec67f">IMFTrackedSample</a>
 

 

