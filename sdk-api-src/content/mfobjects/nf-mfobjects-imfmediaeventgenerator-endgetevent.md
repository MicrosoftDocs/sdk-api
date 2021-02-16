---
UID: NF:mfobjects.IMFMediaEventGenerator.EndGetEvent
title: IMFMediaEventGenerator::EndGetEvent (mfobjects.h)
description: Completes an asynchronous request for the next event in the queue.
helpviewer_keywords: ["6b38e984-d818-4f69-af28-8b54153faebb","EndGetEvent","EndGetEvent method [Media Foundation]","EndGetEvent method [Media Foundation]","IMFMediaEventGenerator interface","IMFMediaEventGenerator interface [Media Foundation]","EndGetEvent method","IMFMediaEventGenerator.EndGetEvent","IMFMediaEventGenerator::EndGetEvent","mf.imfmediaeventgenerator_endgetevent","mfobjects/IMFMediaEventGenerator::EndGetEvent"]
old-location: mf\imfmediaeventgenerator_endgetevent.htm
tech.root: mf
ms.assetid: 6b38e984-d818-4f69-af28-8b54153faebb
ms.date: 12/05/2018
ms.keywords: 6b38e984-d818-4f69-af28-8b54153faebb, EndGetEvent, EndGetEvent method [Media Foundation], EndGetEvent method [Media Foundation],IMFMediaEventGenerator interface, IMFMediaEventGenerator interface [Media Foundation],EndGetEvent method, IMFMediaEventGenerator.EndGetEvent, IMFMediaEventGenerator::EndGetEvent, mf.imfmediaeventgenerator_endgetevent, mfobjects/IMFMediaEventGenerator::EndGetEvent
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
 - IMFMediaEventGenerator::EndGetEvent
 - mfobjects/IMFMediaEventGenerator::EndGetEvent
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
 - IMFMediaEventGenerator.EndGetEvent
---

# IMFMediaEventGenerator::EndGetEvent


## -description

Completes an asynchronous request for the next event in the queue.

## -parameters

### -param pResult [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">Invoke</a> method.

### -param ppEvent [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent">IMFMediaEvent</a> interface. The caller must release the interface.

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

Call this method from inside your application's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method. For example code, see <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent">IMFMediaEventGenerator::BeginGetEvent</a>.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a>



<a href="/windows/desktop/medfound/media-event-generators">Media Event Generators</a>