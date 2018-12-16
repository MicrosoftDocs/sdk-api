---
UID: NN:tuner.IBroadcastEvent
title: IBroadcastEvent
author: windows-sdk-content
description: The IBroadcastEvent interface enables an object to receive events from another object without setting up a direct connection point. Applications typically do not need to use this interface.
old-location: mstv\ibroadcastevent.htm
tech.root: mstv
ms.assetid: 90d4fbc7-d552-460b-96b2-77e2347af716
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBroadcastEvent, IBroadcastEvent interface [Microsoft TV Technologies], IBroadcastEvent interface [Microsoft TV Technologies],described, IBroadcastEventInterface, mstv.ibroadcastevent, tuner/IBroadcastEvent
ms.topic: interface
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IBroadcastEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBroadcastEvent interface


## -description



The <b>IBroadcastEvent</b> interface enables an object to receive events from another object without setting up a direct connection point. Applications typically do not need to use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBroadcastEvent</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBroadcastEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBroadcastEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/974b42d7-bf68-426b-a146-4e520cac3274">Fire</a>
</td>
<td align="left" width="63%">
Fires an event.

</td>
</tr>
</table> 


## -remarks



Broadcast events enable communication among DirectShow filters, Video Control features, and Video Control device objects. To send a broadcast event, an object calls <a href="https://msdn.microsoft.com/974b42d7-bf68-426b-a146-4e520cac3274">IBroadcastEvent::Fire</a> on the <a href="https://msdn.microsoft.com/17c59540-d688-4853-937d-8d9da4b2c732">Broadcast Event Service</a> object. Other objects can listen for events by setting up a connection point with the Broadcast Event Service object. The listener implements <b>IBroadcastEvent</b> and the Broadcast Event Service object calls the listener's <b>Fire</b> method whenever there is a new broadcast event.

Broadcast events are useful for several reasons:

<ul>
<li>The DirectShow event mechanism, <a href="https://msdn.microsoft.com/en-us/library/Dd406901(v=VS.85).aspx">IMediaEventSink</a>, does not support multiple listeners. DirectShow events go onto a queue, and retrieving an event removes it from the queue.</li>
<li>COM connection points require the sink object to locate the source object. With broadcast events, the Broadcast Event Service acts as a relay between the source object and the sink object.</li>
<li>In a connection point, the source must fire events on the same thread that the sink used to establish the connection, or else marshal the event interface pointer. Filter graphs are multithreaded, so the Broadcast Event Service object implements the necessary marshaling. It uses a background thread to distribute events to all the registered listeners.</li>
</ul>
The <b>IBroadcastEvent</b> interface is a service, which can be obtained through the Filter Graph Manager's <b>IServiceProvider</b> interface. To do so, call <b>IServiceProvider::QueryService</b> and specify the following values:

<ul>
<li>Service identifier: SID_SBroadcastEventService</li>
<li>Interface identifier: IID_IBroadcastEvent</li>
</ul>
A failure code from <b>QueryService</b> indicates that no object has yet registered the Broadcast Event Service object with the Filter Graph Manager. In that case, do the following:

<ol>
<li>Create a new Broadcast Event Service object, using <b>CoCreateInstance</b>.</li>
<li>Query the Filter Graph Manager for <a href="https://msdn.microsoft.com/en-us/library/Dd376936(v=VS.85).aspx">IRegisterServiceProvider</a>.</li>
<li>Call <a href="https://msdn.microsoft.com/en-us/library/Dd376937(v=VS.85).aspx">IRegisterServiceProvider::RegisterService</a> with the service identifier.</li>
</ol>
Once you have a pointer to the <b>IBroadcastEvent</b> interface, you can use it either to send events or to sink events. To send events, call the <a href="https://msdn.microsoft.com/974b42d7-bf68-426b-a146-4e520cac3274">Fire</a> method. To sink events, implement <b>IBroadcastEvent</b> on the sink object, query the Broadcast Event Service for <b>IConnectionPoint</b>, and call <b>IConnectionPoint::Advise</b> to establish the connection. For a list of defined broadcast events, see <b>IBroadcastEvent::Fire</b>.

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBroadcastEvent)</code>.


#### Examples

The following example implements a class that can source or sink broadcast events:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
class TunerEvent : public IBroadcastEvent
{

private:
    long m_nRefCount; // Holds the reference count.
public:
    // IUnknown methods
    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&amp;m_nRefCount);
    }
    STDMETHODIMP_(ULONG) Release()
    {
        _ASSERT(m_nRefCount &gt;= 0);
        ULONG uCount = InterlockedDecrement(&amp;m_nRefCount);
        if (uCount == 0)
        {
            delete this;
        }
        // Return the temporary variable, not the member
        // variable, for thread safety.
        return uCount;
    }
    STDMETHODIMP QueryInterface(REFIID riid, void **ppvObject)
    {
        if (NULL == ppvObject)
            return E_POINTER;
        if (riid == __uuidof(IUnknown))
            *ppvObject = static_cast&lt;IUnknown*&gt;(this);
        else if (riid == __uuidof(IBroadcastEvent))
            *ppvObject = static_cast&lt;IBroadcastEvent*&gt;(this);
        else 
            return E_NOINTERFACE;
        AddRef();
        return S_OK;
    }

    // The one IBroadcastEvent method.
    STDMETHOD(Fire)(GUID eventID)
    {
        // The one defined event.
        if (eventID == EVENTID_TuningChanged)
        {
            // The tuner changed stations or channels.
        }
        
        return S_OK;
    }

    TunerEvent() : m_dwBroadcastEventCookie(0), m_nRefCount(1) {};

private:
    HRESULT HookupGraphEventService(IFilterGraph *pGraph);
    HRESULT RegisterForTunerEvents();
    HRESULT UnRegisterForTunerEvents();
    HRESULT Fire_Event(GUID eventID);

    CComPtr&lt;IBroadcastEvent&gt;   m_spBroadcastEvent; 
    DWORD m_dwBroadcastEventCookie;
};

// Query the Filter Graph Manager for the broadcast event service.
// If not found, create it and register it.
HRESULT TunerEvent::HookupGraphEventService(IFilterGraph *pGraph)
{
    HRESULT hr = S_OK;
    if (!m_spBroadcastEvent)
    {
        CComQIPtr&lt;IServiceProvider&gt; spServiceProvider(pGraph);
        if (!spServiceProvider)
        {
            return E_NOINTERFACE;
        }
        hr = spServiceProvider-&gt;QueryService(SID_SBroadcastEventService, 
            IID_IBroadcastEvent, 
            reinterpret_cast&lt;void**&gt;(&amp;m_spBroadcastEvent));
        if (FAILED(hr))
        {
            // Create the Broadcast Event Service object.
            hr = m_spBroadcastEvent.CoCreateInstance(
                CLSID_BroadcastEventService,
                NULL, CLSCTX_INPROC_SERVER);
            if (FAILED(hr))
            {
                return hr; 
            }
            
            CComQIPtr&lt;IRegisterServiceProvider&gt; spRegService(pGraph);
            if (!spRegService)
            {
                return E_NOINTERFACE;
            }
            
            // Register the Broadcast Event Service object as a service.
            hr = spRegService-&gt;RegisterService(
                SID_SBroadcastEventService,
                m_spBroadcastEvent);
        }
    }
    return hr;
}

// Establish the connection point to receive events.
HRESULT TunerEvent::RegisterForTunerEvents()
{
    if (!m_spBroadcastEvent)
    {
        return E_FAIL;  // Forgot to call HookupGraphEventService.
    }
    if(m_dwBroadcastEventCookie)
    {
        return S_FALSE;  // There is already a connection; nothing to do.
    }
    CComQIPtr&lt;IConnectionPoint&gt; spConnectionPoint(m_spBroadcastEvent);
    if(!spConnectionPoint)
    {
        return E_NOINTERFACE;
    }
    return spConnectionPoint-&gt;Advise(static_cast&lt;IBroadcastEvent*&gt;(this),
        &amp;m_dwBroadcastEventCookie);
}

// Unregister for events.
HRESULT TunerEvent::UnRegisterForTunerEvents()
{
    HRESULT hr = S_OK;
    if(!m_dwBroadcastEventCookie)
    {
        return S_OK; // Not registered for events; nothing to do.
    }
    CComQIPtr&lt;IConnectionPoint&gt; spConnectionPoint(m_spBroadcastEvent);
    if(!spConnectionPoint)
    {
        return E_NOINTERFACE;
    }
    
    // Release the connection point.
    hr = spConnectionPoint-&gt;Unadvise(m_dwBroadcastEventCookie);
    if (FAILED(hr))
    {
        // Error: Unable to unadvise the connection point.
        return hr;
    }
    m_dwBroadcastEventCookie = 0;
    m_spBroadcastEvent.Release();
    return S_OK;
}

// Send an event (for source objects).
HRESULT TunerEvent::Fire_Event(GUID eventID)
{
    if (!m_spBroadcastEvent)
    {
        return E_FAIL; // Forgot to call HookupGraphEventService.
    }
    return m_spBroadcastEvent-&gt;Fire(eventID);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

