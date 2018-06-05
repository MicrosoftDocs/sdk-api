---
UID: NF:mfobjects.IMFMediaEventGenerator.BeginGetEvent
title: IMFMediaEventGenerator::BeginGetEvent
author: windows-sdk-content
description: Begins an asynchronous request for the next event in the queue.
old-location: mf\imfmediaeventgenerator_begingetevent.htm
old-project: medfound
ms.assetid: a2afddac-46e9-4928-8b5b-44f3fc7c33d3
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: BeginGetEvent, BeginGetEvent method [Media Foundation], BeginGetEvent method [Media Foundation],IMFMediaEventGenerator interface, IMFMediaEventGenerator interface [Media Foundation],BeginGetEvent method, IMFMediaEventGenerator.BeginGetEvent, IMFMediaEventGenerator::BeginGetEvent, a2afddac-46e9-4928-8b5b-44f3fc7c33d3, mf.imfmediaeventgenerator_begingetevent, mfobjects/IMFMediaEventGenerator::BeginGetEvent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MF_FILE_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFMediaEventGenerator.BeginGetEvent
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEventGenerator::BeginGetEvent


## -description



Begins an asynchronous request for the next event in the queue.




## -parameters




### -param pCallback [in]

Pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface of a callback object. The client must implement this interface.


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



When a new event is available, the event generator calls the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method. The <b>Invoke</b> method should call <a href="https://msdn.microsoft.com/6b38e984-d818-4f69-af28-8b54153faebb">IMFMediaEventGenerator::EndGetEvent</a> to get a pointer to the <a href="https://msdn.microsoft.com/b4f686be-9472-433c-b983-6c48dfd3ac76">IMFMediaEvent</a> interface, and use that interface to examine the event.

Do not call <b>BeginGetEvent</b> a second time before calling <a href="https://msdn.microsoft.com/6b38e984-d818-4f69-af28-8b54153faebb">EndGetEvent</a>. While the first call is still pending, additional calls to the same object will fail. Also, the <a href="https://msdn.microsoft.com/e78464b5-ec6b-4739-a135-352fa297916a">IMFMediaEventGenerator::GetEvent</a> method fails if an asynchronous request is still pending.


#### Examples

The following code shows a typical implementation of <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> for the <b>BeginGetEvent</b> method. The <b>Invoke</b> method calls <a href="https://msdn.microsoft.com/6b38e984-d818-4f69-af28-8b54153faebb">EndGetEvent</a> to get the event data. Then it calls <b>BeginGetEvent</b> again to request another event.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>//////////////////////////////////////////////////////////////////////
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
    hr = m_pEventGenerator-&gt;EndGetEvent(pAsyncResult, &amp;pEvent);

    // Get the event type.
    if (SUCCEEDED(hr))
    {
        hr = pEvent-&gt;GetType(&amp;meType);
    }

    // Get the event status. If the operation that triggered the event 
    // did not succeed, the status is a failure code.
    if (SUCCEEDED(hr))
    {
        hr = pEvent-&gt;GetStatus(&amp;hrStatus);
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
        hr = m_pEventGenerator-&gt;BeginGetEvent(this, NULL);
    }

    SAFE_RELEASE(pEvent);
    return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/a37d0840-c896-43a0-b3d1-c2a6aaff1b25">IMFMediaEventGenerator</a>



<a href="https://msdn.microsoft.com/2e003ad4-9fcb-4834-a335-e4969ffd3a00">Media Event Generators</a>
 

 

