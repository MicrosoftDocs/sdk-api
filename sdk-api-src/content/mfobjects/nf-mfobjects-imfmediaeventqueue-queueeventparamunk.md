---
UID: NF:mfobjects.IMFMediaEventQueue.QueueEventParamUnk
title: IMFMediaEventQueue::QueueEventParamUnk (mfobjects.h)
description: Creates an event, sets an IUnknown pointer as the event data, and puts the event in the queue.
helpviewer_keywords: ["IMFMediaEventQueue interface [Media Foundation]","QueueEventParamUnk method","IMFMediaEventQueue.QueueEventParamUnk","IMFMediaEventQueue::QueueEventParamUnk","QueueEventParamUnk","QueueEventParamUnk method [Media Foundation]","QueueEventParamUnk method [Media Foundation]","IMFMediaEventQueue interface","e51653a4-8f71-44f3-90e8-2052db521307","mf.imfmediaeventqueue_queueeventparamunk","mfobjects/IMFMediaEventQueue::QueueEventParamUnk"]
old-location: mf\imfmediaeventqueue_queueeventparamunk.htm
tech.root: mf
ms.assetid: e51653a4-8f71-44f3-90e8-2052db521307
ms.date: 12/05/2018
ms.keywords: IMFMediaEventQueue interface [Media Foundation],QueueEventParamUnk method, IMFMediaEventQueue.QueueEventParamUnk, IMFMediaEventQueue::QueueEventParamUnk, QueueEventParamUnk, QueueEventParamUnk method [Media Foundation], QueueEventParamUnk method [Media Foundation],IMFMediaEventQueue interface, e51653a4-8f71-44f3-90e8-2052db521307, mf.imfmediaeventqueue_queueeventparamunk, mfobjects/IMFMediaEventQueue::QueueEventParamUnk
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
 - IMFMediaEventQueue::QueueEventParamUnk
 - mfobjects/IMFMediaEventQueue::QueueEventParamUnk
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
 - IMFMediaEventQueue.QueueEventParamUnk
---

# IMFMediaEventQueue::QueueEventParamUnk


## -description

Creates an event, sets an <b>IUnknown</b> pointer as the event data, and puts the event in the queue.

## -parameters

### -param met [in]

Specifies the event type of the event to be added to the queue. The event type is returned by the event's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype">IMFMediaEvent::GetType</a> method. For a list of event types, see <a href="/windows/desktop/medfound/media-foundation-events">Media Foundation Events</a>.

### -param guidExtendedType [in]

The extended type of the event. If the event does not have an extended type, use the value GUID_NULL. The extended type is returned by the event's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype">IMFMediaEvent::GetExtendedType</a> method.

### -param hrStatus [in]

A success or failure code indicating the status of the event. This value is returned by the event's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus">IMFMediaEvent::GetStatus</a> method.

### -param pUnk [in]

Pointer to the <b>IUnknown</b> interface. The method sets this pointer as the event value. The pointer is returned by the event's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue">IMFMediaEvent::GetValue</a> method.

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

Call this method when your component needs to raise an event that contains an <b>IUnknown</b> pointer value and no attributes. If the event contains attributes, use <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent">IMFMediaEventQueue::QueueEvent</a> instead.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue">IMFMediaEventQueue</a>