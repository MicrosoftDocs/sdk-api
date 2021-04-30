---
UID: NF:mfobjects.IMFMediaEventGenerator.QueueEvent
title: IMFMediaEventGenerator::QueueEvent (mfobjects.h)
description: Puts a new event in the object's queue.
helpviewer_keywords: ["3bc33665-1385-41e1-9ad0-991fc93e91c0","IMFMediaEventGenerator interface [Media Foundation]","QueueEvent method","IMFMediaEventGenerator.QueueEvent","IMFMediaEventGenerator::QueueEvent","QueueEvent","QueueEvent method [Media Foundation]","QueueEvent method [Media Foundation]","IMFMediaEventGenerator interface","mf.imfmediaeventgenerator_queueevent","mfobjects/IMFMediaEventGenerator::QueueEvent"]
old-location: mf\imfmediaeventgenerator_queueevent.htm
tech.root: mf
ms.assetid: 3bc33665-1385-41e1-9ad0-991fc93e91c0
ms.date: 12/05/2018
ms.keywords: 3bc33665-1385-41e1-9ad0-991fc93e91c0, IMFMediaEventGenerator interface [Media Foundation],QueueEvent method, IMFMediaEventGenerator.QueueEvent, IMFMediaEventGenerator::QueueEvent, QueueEvent, QueueEvent method [Media Foundation], QueueEvent method [Media Foundation],IMFMediaEventGenerator interface, mf.imfmediaeventgenerator_queueevent, mfobjects/IMFMediaEventGenerator::QueueEvent
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
 - IMFMediaEventGenerator::QueueEvent
 - mfobjects/IMFMediaEventGenerator::QueueEvent
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
 - IMFMediaEventGenerator.QueueEvent
---

# IMFMediaEventGenerator::QueueEvent


## -description

Puts a new event in the object's queue.

## -parameters

### -param met [in]

Specifies the event type. The event type is returned by the event's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype">IMFMediaEvent::GetType</a> method. For a list of event types, see <a href="/windows/desktop/medfound/media-foundation-events">Media Foundation Events</a>.

### -param guidExtendedType [in]

The extended type. If the event does not have an extended type, use the value GUID_NULL. The extended type is returned by the event's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype">IMFMediaEvent::GetExtendedType</a> method.

### -param hrStatus [in]

A success or failure code indicating the status of the event. This value is returned by the event's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus">IMFMediaEvent::GetStatus</a> method.

### -param pvValue [in]

Pointer to a <b>PROPVARIANT</b> that contains the event value. This parameter can be <b>NULL</b>. This value is returned by the event's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue">IMFMediaEvent::GetValue</a> method.

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

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a>



<a href="/windows/desktop/medfound/media-event-generators">Media Event Generators</a>