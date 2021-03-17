---
UID: NF:mfobjects.IMFMediaEventQueue.QueueEvent
title: IMFMediaEventQueue::QueueEvent (mfobjects.h)
description: Puts an event in the queue.
helpviewer_keywords: ["IMFMediaEventQueue interface [Media Foundation]","QueueEvent method","IMFMediaEventQueue.QueueEvent","IMFMediaEventQueue::QueueEvent","QueueEvent","QueueEvent method [Media Foundation]","QueueEvent method [Media Foundation]","IMFMediaEventQueue interface","eb04ce9f-fb64-438f-ad4d-ba1fb849d59c","mf.imfmediaeventqueue_queueevent","mfobjects/IMFMediaEventQueue::QueueEvent"]
old-location: mf\imfmediaeventqueue_queueevent.htm
tech.root: mf
ms.assetid: eb04ce9f-fb64-438f-ad4d-ba1fb849d59c
ms.date: 12/05/2018
ms.keywords: IMFMediaEventQueue interface [Media Foundation],QueueEvent method, IMFMediaEventQueue.QueueEvent, IMFMediaEventQueue::QueueEvent, QueueEvent, QueueEvent method [Media Foundation], QueueEvent method [Media Foundation],IMFMediaEventQueue interface, eb04ce9f-fb64-438f-ad4d-ba1fb849d59c, mf.imfmediaeventqueue_queueevent, mfobjects/IMFMediaEventQueue::QueueEvent
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
 - IMFMediaEventQueue::QueueEvent
 - mfobjects/IMFMediaEventQueue::QueueEvent
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
 - IMFMediaEventQueue.QueueEvent
---

# IMFMediaEventQueue::QueueEvent


## -description

Puts an event in the queue.

## -parameters

### -param pEvent [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent">IMFMediaEvent</a> interface of the event to be put in the queue.

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

Call this method when your component needs to raise an event that contains attributes. To create the event object, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediaevent">MFCreateMediaEvent</a>. Add attributes to the event by using methods from the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface. (The <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent">IMFMediaEvent</a> interface inherits <b>IMFAttributes</b>.)

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue">IMFMediaEventQueue</a>