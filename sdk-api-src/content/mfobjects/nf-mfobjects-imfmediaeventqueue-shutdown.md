---
UID: NF:mfobjects.IMFMediaEventQueue.Shutdown
title: IMFMediaEventQueue::Shutdown (mfobjects.h)
description: Shuts down the event queue.
helpviewer_keywords: ["6ec52973-0d90-463b-b2be-08d5d6fdcc05","IMFMediaEventQueue interface [Media Foundation]","Shutdown method","IMFMediaEventQueue.Shutdown","IMFMediaEventQueue::Shutdown","Shutdown","Shutdown method [Media Foundation]","Shutdown method [Media Foundation]","IMFMediaEventQueue interface","mf.imfmediaeventqueue_shutdown","mfobjects/IMFMediaEventQueue::Shutdown"]
old-location: mf\imfmediaeventqueue_shutdown.htm
tech.root: mf
ms.assetid: 6ec52973-0d90-463b-b2be-08d5d6fdcc05
ms.date: 12/05/2018
ms.keywords: 6ec52973-0d90-463b-b2be-08d5d6fdcc05, IMFMediaEventQueue interface [Media Foundation],Shutdown method, IMFMediaEventQueue.Shutdown, IMFMediaEventQueue::Shutdown, Shutdown, Shutdown method [Media Foundation], Shutdown method [Media Foundation],IMFMediaEventQueue interface, mf.imfmediaeventqueue_shutdown, mfobjects/IMFMediaEventQueue::Shutdown
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
 - IMFMediaEventQueue::Shutdown
 - mfobjects/IMFMediaEventQueue::Shutdown
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
 - IMFMediaEventQueue.Shutdown
---

# IMFMediaEventQueue::Shutdown


## -description

Shuts down the event queue.



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
</table>

## -remarks

Call this method when your component shuts down. After this method is called, all <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue">IMFMediaEventQueue</a> methods return <b>MF_E_SHUTDOWN</b>.

This method removes all of the events from the queue.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue">IMFMediaEventQueue</a>
