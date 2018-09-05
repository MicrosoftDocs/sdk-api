---
UID: NN:wbemcli.IWbemObjectSink
title: IWbemObjectSink
author: windows-sdk-content
description: The IWbemObjectSink interface creates a sink interface that can receive all types of notifications within the WMI programming model.
old-location: wmi\iwbemobjectsink.htm
old-project: WmiSdk
ms.assetid: 987aea1d-912a-4691-987f-181c1ef1a8a9
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: IWbemObjectSink, IWbemObjectSink interface [Windows Management Instrumentation], IWbemObjectSink interface [Windows Management Instrumentation],described, _hmm_iwbemobjectsink, wbemcli/IWbemObjectSink, wmi.iwbemobjectsink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: WMI_OBJ_TEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fastprox.dll
api_name:
 - IWbemObjectSink
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemObjectSink interface


## -description


The 
<b>IWbemObjectSink</b> interface creates a sink interface that can receive all types of notifications within the WMI programming model. Clients must implement this interface to receive both the results of the 
<a href="https://msdn.microsoft.com/5179969f-bc7d-4408-84ef-7b003950a59f">asynchronous methods</a> of 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a>, and specific types of event notifications. Providers use, but do not implement this interface to provide events and objects to WMI.

Typically, providers call an implementation provided to them by WMI. In these cases, call 
<a href="https://msdn.microsoft.com/96756b27-cbcf-47ce-a8c8-88795a81edde">Indicate</a> to provide objects to the WMI service. After that, call 
<a href="https://msdn.microsoft.com/e47e8cd9-4e80-45c4-b1f0-2f68aea4eb7b">SetStatus</a> to indicate the end of the notification sequence. You can also call 
<b>SetStatus</b> to indicate errors when the sink does not have any objects.

When programming asynchronous clients of WMI, the user provides the implementation. WMI calls the methods to deliver objects and set the status of the result.
<div class="alert"><b>Note</b>  If a client application passes the same sink interface in two different overlapping asynchronous calls, WMI does not guarantee the order of the callback. Client applications that make overlapping asynchronous calls should either pass different sink objects, or  serialize their calls.</div><div> </div><div class="alert"><b>Note</b>  Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.  For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemObjectSink</b> interface has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemObjectSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96756b27-cbcf-47ce-a8c8-88795a81edde">Indicate</a>
</td>
<td align="left" width="63%">
Receives notification objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e47e8cd9-4e80-45c4-b1f0-2f68aea4eb7b">SetStatus</a>
</td>
<td align="left" width="63%">
Called by sources  to indicate the end of a notification sequence, or to send other status codes to the sink.

</td>
</tr>
</table> 


## -remarks



When implementing an event subscription sink (<b>IWbemObjectSink</b> or <a href="https://msdn.microsoft.com/dd076dd0-ed39-47a2-86fb-a595baf3f464">IWbemEventSink</a>), do  not call into WMI from within the <a href="https://msdn.microsoft.com/96756b27-cbcf-47ce-a8c8-88795a81edde">Indicate</a>  or <a href="https://msdn.microsoft.com/e47e8cd9-4e80-45c4-b1f0-2f68aea4eb7b">SetStatus</a>methods on the sink object.  For example, calling <a href="https://msdn.microsoft.com/803a7831-1e3d-4940-8d2b-1a74dd16f51a">IWbemServices::CancelAsyncCall</a> to cancel the sink  from within an implementation of <a href="https://msdn.microsoft.com/96756b27-cbcf-47ce-a8c8-88795a81edde">Indicate</a> can interfere with the WMI state. To cancel an event subscription, set a flag and call <b>IWbemServices::CancelAsyncCall</b> from another thread or object. For implementations that are not related to an event sink, such as object, enum, and query retrievals, you can call back into WMI.

Sink implementations should process the event notification within 100 MSEC because the WMI thread that delivers the event notification cannot do other work until the sink object has completed processing. If the notification requires a large amount of processing, the sink can use an internal queue for another thread to handle the processing.


#### Examples

The following code example is a simple implementation of an object sink. This sample can be used  with 
<a href="https://msdn.microsoft.com/d8b55500-d84c-431b-93c6-99d1f1b845c3">IWbemServices::ExecQueryAsync</a> or 
<a href="https://msdn.microsoft.com/5ba2ff28-034f-4949-9bde-8c98345ec7c6">IWbemServices::CreateInstanceEnumAsync</a> to receive the returned instances:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;iostream&gt;
#include &lt;wbemidl.h&gt;
#pragma comment(lib, "wbemuuid.lib")

class QuerySink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone; 

public:
    QuerySink() { m_lRef = 0; }
   ~QuerySink() { bDone = TRUE; }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT STDMETHODCALLTYPE 
        QueryInterface(REFIID riid, void** ppv);

    virtual HRESULT STDMETHODCALLTYPE Indicate( 
            /* [in] */
            LONG lObjectCount,
            /* [size_is][in] */
            IWbemClassObject __RPC_FAR *__RPC_FAR *apObjArray
            );
        
    virtual HRESULT STDMETHODCALLTYPE SetStatus( 
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
            );
};


ULONG QuerySink::AddRef()
{
    return InterlockedIncrement(&amp;m_lRef);
}

ULONG QuerySink::Release()
{
    LONG lRef = InterlockedDecrement(&amp;m_lRef);
    if(lRef == 0)
        delete this;
    return lRef;
}

HRESULT QuerySink::QueryInterface(REFIID riid, void** ppv)
{
    if (riid == IID_IUnknown || riid == IID_IWbemObjectSink)
    {
        *ppv = (IWbemObjectSink *) this;
        AddRef();
        return WBEM_S_NO_ERROR;
    }
    else return E_NOINTERFACE;
}


HRESULT QuerySink::Indicate(long lObjCount, IWbemClassObject **pArray)
{
    for (long i = 0; i &lt; lObjCount; i++)
    {
        IWbemClassObject *pObj = pArray[i];

        // ... use the object.

        // AddRef() is only required if the object will be held after
        // the return to the caller.
    }

    return WBEM_S_NO_ERROR;
}

HRESULT QuerySink::SetStatus(
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
        )
{
    printf("QuerySink::SetStatus hResult = 0x%X\n", hResult);
    return WBEM_S_NO_ERROR;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5fa8f1b5-fd19-4d45-9b53-bc7089eecdb1">COM API for WMI</a>



<a href="https://msdn.microsoft.com/5179969f-bc7d-4408-84ef-7b003950a59f">Making an Asynchronous Call with C++</a>



<a href="https://msdn.microsoft.com/380ac556-ba0a-4fae-8b76-0645d99e8583">Receiving Events for the Duration of your Application</a>



<a href="https://msdn.microsoft.com/2b839ea9-e1e6-4123-a98a-04ebee907b3b">Setting Security on an Asynchronous Call</a>
 

 

