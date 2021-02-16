---
UID: NF:mfobjects.IMFMediaEventQueue.GetEvent
title: IMFMediaEventQueue::GetEvent (mfobjects.h)
description: Retrieves the next event in the queue. This method is synchronous.Call this method inside your implementation of IMFMediaEventGenerator::GetEvent. Pass the parameters from that method directly to this method.
helpviewer_keywords: ["GetEvent","GetEvent method [Media Foundation]","GetEvent method [Media Foundation]","IMFMediaEventQueue interface","IMFMediaEventQueue interface [Media Foundation]","GetEvent method","IMFMediaEventQueue.GetEvent","IMFMediaEventQueue::GetEvent","b7c48607-f410-47ee-8cc6-38123919da55","mf.imfmediaeventqueue_getevent","mfobjects/IMFMediaEventQueue::GetEvent"]
old-location: mf\imfmediaeventqueue_getevent.htm
tech.root: mf
ms.assetid: b7c48607-f410-47ee-8cc6-38123919da55
ms.date: 12/05/2018
ms.keywords: GetEvent, GetEvent method [Media Foundation], GetEvent method [Media Foundation],IMFMediaEventQueue interface, IMFMediaEventQueue interface [Media Foundation],GetEvent method, IMFMediaEventQueue.GetEvent, IMFMediaEventQueue::GetEvent, b7c48607-f410-47ee-8cc6-38123919da55, mf.imfmediaeventqueue_getevent, mfobjects/IMFMediaEventQueue::GetEvent
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
 - IMFMediaEventQueue::GetEvent
 - mfobjects/IMFMediaEventQueue::GetEvent
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
 - IMFMediaEventQueue.GetEvent
---

# IMFMediaEventQueue::GetEvent


## -description

Retrieves the next event in the queue. This method is synchronous.

Call this method inside your implementation of <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent">IMFMediaEventGenerator::GetEvent</a>. Pass the parameters from that method directly to this method.

## -parameters

### -param dwFlags [in]

Specifies whether the method blocks until an event is queued. For a list of valid flags, see <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent">IMFMediaEventGenerator::GetEvent</a>.

### -param ppEvent [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent">IMFMediaEvent</a> interface.

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