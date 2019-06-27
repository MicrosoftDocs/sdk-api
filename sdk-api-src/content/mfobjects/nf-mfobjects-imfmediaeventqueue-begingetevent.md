---
UID: NF:mfobjects.IMFMediaEventQueue.BeginGetEvent
title: IMFMediaEventQueue::BeginGetEvent (mfobjects.h)
author: windows-sdk-content
description: Begins an asynchronous request for the next event in the queue.Call this method inside your implementation of IMFMediaEventGenerator::BeginGetEvent. Pass the parameters from that method directly to this method.
old-location: mf\imfmediaeventqueue_begingetevent.htm
tech.root: medfound
ms.assetid: 454d4b3b-6251-4b7e-b8f3-ff7cff5269b5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 454d4b3b-6251-4b7e-b8f3-ff7cff5269b5, BeginGetEvent, BeginGetEvent method [Media Foundation], BeginGetEvent method [Media Foundation],IMFMediaEventQueue interface, IMFMediaEventQueue interface [Media Foundation],BeginGetEvent method, IMFMediaEventQueue.BeginGetEvent, IMFMediaEventQueue::BeginGetEvent, mf.imfmediaeventqueue_begingetevent, mfobjects/IMFMediaEventQueue::BeginGetEvent
ms.topic: method
f1_keywords: 
 - "mfobjects/IMFMediaEventQueue.BeginGetEvent"
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
 - IMFMediaEventQueue.BeginGetEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEventQueue::BeginGetEvent


## -description



Begins an asynchronous request for the next event in the queue.

Call this method inside your implementation of <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent">IMFMediaEventGenerator::BeginGetEvent</a>. Pass the parameters from that method directly to this method.




## -parameters




### -param pCallback [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface of a callback object.


### -param punkState [in]

Pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. The object is returned to the caller when the callback is invoked.


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
The <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown">Shutdown</a> method was called.

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




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue">IMFMediaEventQueue</a>
 

 

