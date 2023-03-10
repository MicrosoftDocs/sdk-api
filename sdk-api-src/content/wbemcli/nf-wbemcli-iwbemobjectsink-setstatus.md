---
UID: NF:wbemcli.IWbemObjectSink.SetStatus
title: IWbemObjectSink::SetStatus (wbemcli.h)
description: Called by sources to indicate the end of a notification sequence, or to send other status codes to the sink.
helpviewer_keywords: ["IWbemObjectSink interface [Windows Management Instrumentation]","SetStatus method","IWbemObjectSink.SetStatus","IWbemObjectSink::SetStatus","IWbemObjectSinkEx interface [Windows Management Instrumentation]","SetStatus method","IWbemObjectSinkEx::SetStatus","SetStatus","SetStatus method [Windows Management Instrumentation]","SetStatus method [Windows Management Instrumentation]","IWbemObjectSink interface","SetStatus method [Windows Management Instrumentation]","IWbemObjectSinkEx interface","WBEM_STATUS_COMPLETE","WBEM_STATUS_PROGRESS","WBEM_STATUS_REQUIREMENTS","_hmm_iwbemobjectsink_setstatus","wbemcli/IWbemObjectSink::SetStatus","wbemcli/IWbemObjectSinkEx::SetStatus","wmi.iwbemobjectsink_setstatus"]
old-location: wmi\iwbemobjectsink_setstatus.htm
tech.root: wmi
ms.assetid: e47e8cd9-4e80-45c4-b1f0-2f68aea4eb7b
ms.date: 12/05/2018
ms.keywords: IWbemObjectSink interface [Windows Management Instrumentation],SetStatus method, IWbemObjectSink.SetStatus, IWbemObjectSink::SetStatus, IWbemObjectSinkEx interface [Windows Management Instrumentation],SetStatus method, IWbemObjectSinkEx::SetStatus, SetStatus, SetStatus method [Windows Management Instrumentation], SetStatus method [Windows Management Instrumentation],IWbemObjectSink interface, SetStatus method [Windows Management Instrumentation],IWbemObjectSinkEx interface, WBEM_STATUS_COMPLETE, WBEM_STATUS_PROGRESS, WBEM_STATUS_REQUIREMENTS, _hmm_iwbemobjectsink_setstatus, wbemcli/IWbemObjectSink::SetStatus, wbemcli/IWbemObjectSinkEx::SetStatus, wmi.iwbemobjectsink_setstatus
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
 - IWbemObjectSink::SetStatus
 - wbemcli/IWbemObjectSink::SetStatus
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
 - IWbemObjectSink.SetStatus
 - IWbemObjectSinkEx.SetStatus
---

# IWbemObjectSink::SetStatus


## -description

The 
<b>IWbemObjectSink::SetStatus</b> method is called by sources  to indicate the end of a notification sequence, or to send other status codes to the sink. The 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">IWbemObjectSink::Indicate</a> method may or may not have been called before the call to 
<b>SetStatus</b>.

Typically, a client implements the 
<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a> interface, and executes 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> methods that return their results using the 
<b>IWbemObjectSink</b> interface. During this operation, WMI calls 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">Indicate</a> as many times as required, followed by a final call to 
<b>SetStatus</b>, and in many cases, <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>.

## -parameters

### -param lFlags [in]

Bitmask of status information. The status of the operation can be obtained by examining the <i>hResult</i> parameter.



#### WBEM_STATUS_COMPLETE

The operation has completed.



#### WBEM_STATUS_PROGRESS

The operation is still in progress.



#### WBEM_STATUS_REQUIREMENTS

Used in activating post-filtering.

### -param hResult [in]

This parameter is set to the <b>HRESULT</b> of the asynchronous operation or notification. This is either an error code, if an error occurred, or the amount of progress that has been made on an asynchronous call.

### -param strParam [in]

Receives a pointer to a read-only <b>BSTR</b>, if the original asynchronous operation returns a string. For example, when using 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync">PutInstanceAsync</a>, 
<b>SetStatus</b> is called with this parameter set to the object path of the newly created instance.

### -param pObjParam [in]

In cases where a complex error or status object is returned, this contains a pointer to the error object. If the object is required after 
<b>SetStatus</b> returns, the called object must use the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on the pointer before the called object returns.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -remarks

When implementing an event subscription sink (<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a> or <a href="/windows/desktop/WmiSdk/iwbemeventsink">IWbemEventSink</a>), do  not call into WMI from within the <b>SetStatus</b>  method on the sink object.  For example, calling <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-cancelasynccall">IWbemServices::CancelAsyncCall</a>  from within an implementation of <b>SetStatus</b> can interfere with the WMI state. To cancel an event subscription, set a flag and call <b>IWbemServices::CancelAsyncCall</b> from another thread or object. For implementations that are not related to an event sink, such as object, enum, and query retrievals, you can call back into WMI.

Sink implementations should process the event notification within 100 MSEC because the WMI thread that delivers the event notification cannot do other work until the sink object has completed processing. If the notification requires a large amount of processing, the sink can use an internal queue for another thread to handle the processing. For implementations that are not related to an event sink, such as object, enum, and query retrievals, you can call back into WMI.

To receive intermediate status updates through the client's implementation of <b>SetStatus</b>, you must specify <b>WBEM_FLAG_SENT_STATUS</b> in your call to a provider/service method. The exact status can be determined by examining the HIWORD and LOWORD values of <i>hResult</i> separately. The LOWORD (<i>hResult</i>) value contains the amount of progress that has been made so far and the HIWORD (<i>hResult</i>) value contains the total.

If you do not specify <b>WBEM_FLAG_SEND_STATUS</b> when calling your provider or service method, you are guaranteed to receive one and only one call to 
<b>SetStatus</b>.

## -see-also

<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">IWbemObjectSink::Indicate</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectsinkex">IWbemObjectSinkEx</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync">IWbemServices::ExecQueryAsync</a>



<a href="/windows/win32/api/wbemcli/ne-wbemcli-wbem_status_type">WBEM_STATUS_TYPE</a>