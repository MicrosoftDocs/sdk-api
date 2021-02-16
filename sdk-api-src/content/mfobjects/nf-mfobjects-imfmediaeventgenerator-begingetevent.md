---
UID: NF:mfobjects.IMFMediaEventGenerator.BeginGetEvent
title: IMFMediaEventGenerator::BeginGetEvent (mfobjects.h)
description: Begins an asynchronous request for the next event in the queue.
helpviewer_keywords: ["BeginGetEvent","BeginGetEvent method [Media Foundation]","BeginGetEvent method [Media Foundation]","IMFMediaEventGenerator interface","IMFMediaEventGenerator interface [Media Foundation]","BeginGetEvent method","IMFMediaEventGenerator.BeginGetEvent","IMFMediaEventGenerator::BeginGetEvent","a2afddac-46e9-4928-8b5b-44f3fc7c33d3","mf.imfmediaeventgenerator_begingetevent","mfobjects/IMFMediaEventGenerator::BeginGetEvent"]
old-location: mf\imfmediaeventgenerator_begingetevent.htm
tech.root: mf
ms.assetid: a2afddac-46e9-4928-8b5b-44f3fc7c33d3
ms.date: 12/05/2018
ms.keywords: BeginGetEvent, BeginGetEvent method [Media Foundation], BeginGetEvent method [Media Foundation],IMFMediaEventGenerator interface, IMFMediaEventGenerator interface [Media Foundation],BeginGetEvent method, IMFMediaEventGenerator.BeginGetEvent, IMFMediaEventGenerator::BeginGetEvent, a2afddac-46e9-4928-8b5b-44f3fc7c33d3, mf.imfmediaeventgenerator_begingetevent, mfobjects/IMFMediaEventGenerator::BeginGetEvent
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
 - IMFMediaEventGenerator::BeginGetEvent
 - mfobjects/IMFMediaEventGenerator::BeginGetEvent
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
 - IMFMediaEventGenerator.BeginGetEvent
---

# IMFMediaEventGenerator::BeginGetEvent


## -description

Begins an asynchronous request for the next event in the queue.

## -parameters

### -param pCallback [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface of a callback object. The client must implement this interface.

### -param punkState [in]

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_MULTIPLE_BEGIN</b></dt>
</dl>
</td>
<td width="60%">
There is a pending request with the same callback pointer and a different state object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_MULTIPLE_SUBSCRIBERS</b></dt>
</dl>
</td>
<td width="60%">
There is a pending request with a different callback pointer.

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_S_MULTIPLE_BEGIN</b></dt>
</dl>
</td>
<td width="60%">
There is a pending request with the same callback pointer and state object.

</td>
</tr>
</table>

## -remarks

When a new event is available, the event generator calls the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method. The <b>Invoke</b> method should call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent">IMFMediaEventGenerator::EndGetEvent</a> to get a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent">IMFMediaEvent</a> interface, and use that interface to examine the event.

Do not call <b>BeginGetEvent</b> a second time before calling <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent">EndGetEvent</a>. While the first call is still pending, additional calls to the same object will fail. Also, the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent">IMFMediaEventGenerator::GetEvent</a> method fails if an asynchronous request is still pending.


#### Examples

The following code shows a typical implementation of <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> for the <b>BeginGetEvent</b> method. The <b>Invoke</b> method calls <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent">EndGetEvent</a> to get the event data. Then it calls <b>BeginGetEvent</b> again to request another event.


```
//////////////////////////////////////////////////////////////////////
//  Name: CEventHandler::Invoke
//  Callback for asynchronous BeginGetEvent method.
//
//  pAsyncResult: Pointer to the result.
//
//  This code example assumes that CEventHandler is a class that 
//  implements the IMFAsyncCallback interface. 
///////////////////////////////////////////////////////////////////////
HRESULT CEventHandler::Invoke(IMFAsyncResult *pAsyncResult)
{
    HRESULT hr = S_OK;
    IMFMediaEvent* pEvent = NULL;
    MediaEventType meType = MEUnknown;
    BOOL fGetAnotherEvent = TRUE;
    HRESULT hrStatus = S_OK;

    // Get the event from the event queue.
    // Assume that m_pEventGenerator is a valid pointer to the
    // event generator's IMFMediaEventGenerator interface.
    hr = m_pEventGenerator->EndGetEvent(pAsyncResult, &pEvent);

    // Get the event type.
    if (SUCCEEDED(hr))
    {
        hr = pEvent->GetType(&meType);
    }

    // Get the event status. If the operation that triggered the event 
    // did not succeed, the status is a failure code.
    if (SUCCEEDED(hr))
    {
        hr = pEvent->GetStatus(&hrStatus);
    }

    if (SUCCEEDED(hr))
    {
        // TODO: Handle the event.
    }

    // If not finished, request another event.
    // Pass in a pointer to this instance of the application's
    // CEventHandler class, which implements the callback.
    if (fGetAnotherEvent)
    {
        hr = m_pEventGenerator->BeginGetEvent(this, NULL);
    }

    SAFE_RELEASE(pEvent);
    return hr;
}
```

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a>



<a href="/windows/desktop/medfound/media-event-generators">Media Event Generators</a>