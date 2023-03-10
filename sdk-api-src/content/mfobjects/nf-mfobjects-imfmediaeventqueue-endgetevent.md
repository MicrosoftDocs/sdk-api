---
UID: NF:mfobjects.IMFMediaEventQueue.EndGetEvent
title: IMFMediaEventQueue::EndGetEvent (mfobjects.h)
description: Completes an asynchronous request for the next event in the queue.Call this method inside your implementation of IMFMediaEventGenerator::EndGetEvent. Pass the parameters from that method directly to this method.
helpviewer_keywords: ["EndGetEvent","EndGetEvent method [Media Foundation]","EndGetEvent method [Media Foundation]","IMFMediaEventQueue interface","IMFMediaEventQueue interface [Media Foundation]","EndGetEvent method","IMFMediaEventQueue.EndGetEvent","IMFMediaEventQueue::EndGetEvent","bb0ea226-9dc0-43e3-a482-cfec531b5734","mf.imfmediaeventqueue_endgetevent","mfobjects/IMFMediaEventQueue::EndGetEvent"]
old-location: mf\imfmediaeventqueue_endgetevent.htm
tech.root: mf
ms.assetid: bb0ea226-9dc0-43e3-a482-cfec531b5734
ms.date: 12/05/2018
ms.keywords: EndGetEvent, EndGetEvent method [Media Foundation], EndGetEvent method [Media Foundation],IMFMediaEventQueue interface, IMFMediaEventQueue interface [Media Foundation],EndGetEvent method, IMFMediaEventQueue.EndGetEvent, IMFMediaEventQueue::EndGetEvent, bb0ea226-9dc0-43e3-a482-cfec531b5734, mf.imfmediaeventqueue_endgetevent, mfobjects/IMFMediaEventQueue::EndGetEvent
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaEventQueue::EndGetEvent
 - mfobjects/IMFMediaEventQueue::EndGetEvent
dev_langs:
 - c++
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
---

# IMFMediaEventQueue::EndGetEvent


## -description

Completes an asynchronous request for the next event in the queue.

Call this method inside your implementation of <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent">IMFMediaEventGenerator::EndGetEvent</a>. Pass the parameters from that method directly to this method.

## -parameters

### -param pResult [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface.

### -param ppEvent [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent">IMFMediaEvent</a> interface of the event object. The caller must release the interface.

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
The <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown">Shutdown</a> method was called.

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

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue">IMFMediaEventQueue</a>