---
UID: NF:wbemcli.IWbemObjectSink.Indicate
title: IWbemObjectSink::Indicate (wbemcli.h)
description: Called by a source to provide a notification.
helpviewer_keywords: ["IWbemObjectSink interface [Windows Management Instrumentation]","Indicate method","IWbemObjectSink.Indicate","IWbemObjectSink::Indicate","IWbemObjectSinkEx interface [Windows Management Instrumentation]","Indicate method","IWbemObjectSinkEx::Indicate","Indicate","Indicate method [Windows Management Instrumentation]","Indicate method [Windows Management Instrumentation]","IWbemObjectSink interface","Indicate method [Windows Management Instrumentation]","IWbemObjectSinkEx interface","_hmm_iwbemobjectsink_indicate","wbemcli/IWbemObjectSink::Indicate","wbemcli/IWbemObjectSinkEx::Indicate","wmi.iwbemobjectsink_indicate"]
old-location: wmi\iwbemobjectsink_indicate.htm
tech.root: wmi
ms.assetid: 96756b27-cbcf-47ce-a8c8-88795a81edde
ms.date: 12/05/2018
ms.keywords: IWbemObjectSink interface [Windows Management Instrumentation],Indicate method, IWbemObjectSink.Indicate, IWbemObjectSink::Indicate, IWbemObjectSinkEx interface [Windows Management Instrumentation],Indicate method, IWbemObjectSinkEx::Indicate, Indicate, Indicate method [Windows Management Instrumentation], Indicate method [Windows Management Instrumentation],IWbemObjectSink interface, Indicate method [Windows Management Instrumentation],IWbemObjectSinkEx interface, _hmm_iwbemobjectsink_indicate, wbemcli/IWbemObjectSink::Indicate, wbemcli/IWbemObjectSinkEx::Indicate, wmi.iwbemobjectsink_indicate
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
 - IWbemObjectSink::Indicate
 - wbemcli/IWbemObjectSink::Indicate
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
 - IWbemObjectSink.Indicate
 - IWbemObjectSinkEx.Indicate
---

# IWbemObjectSink::Indicate


## -description

The 
<b>Indicate</b> method is called by a source to provide a notification. Typically, WMI calls the client implementation of this interface after the client executes one of the asynchronous methods of 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>. In other cases, various types of providers call an implementation exported by WMI to deliver events. Therefore, client code may have to implement this interface in some cases, and use a different component's implementation in other cases.

Use this interface and method in conjunction with the asynchronous methods of the 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> interface.

Clients and providers must implement this interface to receive notifications or to execute the asynchronous methods of 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>. For more information, see 
<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.

## -parameters

### -param lObjectCount [in]

Number of objects in the following array of pointers.

### -param apObjArray [in]

Array of pointers to 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> interfaces. The array memory itself is read-only, and is owned by the caller of the method. Because this is an in parameter, the implementation has the option of calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IWbemClassObject::AddRef</a> on any object pointer in the array and holding it before returning if the objects will be used after the method has returned, in accordance with COM rules. If the objects are only used for the duration of the 
<b>Indicate</b> call, then you do not need to call <b>AddRef</b> on each object pointer.

## -returns

This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -remarks

When implementing an event subscription sink (<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a> or <a href="/windows/desktop/WmiSdk/iwbemeventsink">IWbemEventSink</a>), do  not call into WMI from within the <b>Indicate</b>  method on the sink object.  For example, calling <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-cancelasynccall">IWbemServices::CancelAsyncCall</a>  from within an implementation of <b>Indicate</b> can interfere with the WMI state. To cancel an event subscription, set a flag and call <b>IWbemServices::CancelAsyncCall</b> from another thread or object. For implementations that are not related to an event sink, such as object, enum, and query retrievals, you can call back into WMI.

Sink implementations should process the event notification within 100 MSEC because the WMI thread that delivers the event notification cannot do other work until the sink object has completed processing. If the notification requires a large amount of processing, the sink can use an internal queue for another thread to handle the processing.

When an event provider calls 
<b>Indicate</b> to provide an event, the call can fail with <b>WBEM_E_SERVER_TOO_BUSY</b>. The provider can choose to respond to this message by re-firing the event.

<div class="alert"><b>Note</b>  Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.  For more information, see <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectsinkex">IWbemObjectSinkEx</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync">IWbemServices::ExecQueryAsync</a>