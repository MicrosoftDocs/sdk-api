---
UID: NN:wbemcli.IWbemObjectSink
title: IWbemObjectSink (wbemcli.h)
description: The IWbemObjectSink interface creates a sink interface that can receive all types of notifications within the WMI programming model.
helpviewer_keywords: ["IWbemObjectSink","IWbemObjectSink interface [Windows Management Instrumentation]","IWbemObjectSink interface [Windows Management Instrumentation]","described","_hmm_iwbemobjectsink","wbemcli/IWbemObjectSink","wmi.iwbemobjectsink"]
old-location: wmi\iwbemobjectsink.htm
tech.root: wmi
ms.assetid: 987aea1d-912a-4691-987f-181c1ef1a8a9
ms.date: 12/05/2018
ms.keywords: IWbemObjectSink, IWbemObjectSink interface [Windows Management Instrumentation], IWbemObjectSink interface [Windows Management Instrumentation],described, _hmm_iwbemobjectsink, wbemcli/IWbemObjectSink, wmi.iwbemobjectsink
req.header: wbemcli.h
req.include-header: Wbemidl.h
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
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemObjectSink
 - wbemcli/IWbemObjectSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fastprox.dll
api_name:
 - IWbemObjectSink
---

# IWbemObjectSink interface


## -description

The 
<b>IWbemObjectSink</b> interface creates a sink interface that can receive all types of notifications within the WMI programming model. Clients must implement this interface to receive both the results of the 
<a href="/windows/desktop/WmiSdk/making-an-asynchronous-call-with-c--">asynchronous methods</a> of 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>, and specific types of event notifications. Providers use, but do not implement this interface to provide events and objects to WMI.

Typically, providers call an implementation provided to them by WMI. In these cases, call 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">Indicate</a> to provide objects to the WMI service. After that, call 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">SetStatus</a> to indicate the end of the notification sequence. You can also call 
<b>SetStatus</b> to indicate errors when the sink does not have any objects.

When programming asynchronous clients of WMI, the user provides the implementation. WMI calls the methods to deliver objects and set the status of the result.
<div class="alert"><b>Note</b>  If a client application passes the same sink interface in two different overlapping asynchronous calls, WMI does not guarantee the order of the callback. Client applications that make overlapping asynchronous calls should either pass different sink objects, or  serialize their calls.</div><div> </div><div class="alert"><b>Note</b>  Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.  For more information, see <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.</div><div> </div>

## -inheritance

The <b>IWbemObjectSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemObjectSink</b> also has these types of members:

## -remarks

When implementing an event subscription sink (<b>IWbemObjectSink</b> or <a href="/windows/desktop/WmiSdk/iwbemeventsink">IWbemEventSink</a>), do  not call into WMI from within the <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">Indicate</a>  or <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">SetStatus</a> methods on the sink object.  For example, calling <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-cancelasynccall">IWbemServices::CancelAsyncCall</a> to cancel the sink  from within an implementation of <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">Indicate</a> can interfere with the WMI state. To cancel an event subscription, set a flag and call <b>IWbemServices::CancelAsyncCall</b> from another thread or object. For implementations that are not related to an event sink, such as object, enum, and query retrievals, you can call back into WMI.

Sink implementations should process the event notification within 100 MSEC because the WMI thread that delivers the event notification cannot do other work until the sink object has completed processing. If the notification requires a large amount of processing, the sink can use an internal queue for another thread to handle the processing.


#### Examples

The following code example is a simple implementation of an object sink. This sample can be used  with 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync">IWbemServices::ExecQueryAsync</a> or 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync">IWbemServices::CreateInstanceEnumAsync</a> to receive the returned instances:

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>

```
#include <iostream>
#include <wbemidl.h>
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
    return InterlockedIncrement(&m_lRef);
}

ULONG QuerySink::Release()
{
    LONG lRef = InterlockedDecrement(&m_lRef);
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
    for (long i = 0; i < lObjCount; i++)
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
}
```
</td>
</tr>
</table></span></div>

## -see-also

<a href="/windows/desktop/WmiSdk/com-api-for-wmi">COM API for WMI</a>



<a href="/windows/desktop/WmiSdk/making-an-asynchronous-call-with-c--">Making an Asynchronous Call with C++</a>



<a href="/windows/desktop/WmiSdk/receiving-events-for-the-duration-of-your-application">Receiving Events for the Duration of your Application</a>



<a href="/windows/desktop/WmiSdk/setting-security-on-an-asynchronous-call">Setting Security on an Asynchronous Call</a>
