---
UID: NF:wbemcli.IWbemServices.CancelAsyncCall
title: IWbemServices::CancelAsyncCall (wbemcli.h)
description: The IWbemServices::CancelAsyncCall method cancels any currently pending asynchronous calls based on the IWbemObjectSink pointer, which was originally passed to the asynchronous method.
helpviewer_keywords: ["CancelAsyncCall","CancelAsyncCall method [Windows Management Instrumentation]","CancelAsyncCall method [Windows Management Instrumentation]","IWbemServices interface","IWbemServices interface [Windows Management Instrumentation]","CancelAsyncCall method","IWbemServices.CancelAsyncCall","IWbemServices::CancelAsyncCall","_hmm_iwbemservices_cancelasynccall","wbemcli/IWbemServices::CancelAsyncCall","wmi.iwbemservices_cancelasynccall"]
old-location: wmi\iwbemservices_cancelasynccall.htm
tech.root: wmi
ms.assetid: 803a7831-1e3d-4940-8d2b-1a74dd16f51a
ms.date: 12/05/2018
ms.keywords: CancelAsyncCall, CancelAsyncCall method [Windows Management Instrumentation], CancelAsyncCall method [Windows Management Instrumentation],IWbemServices interface, IWbemServices interface [Windows Management Instrumentation],CancelAsyncCall method, IWbemServices.CancelAsyncCall, IWbemServices::CancelAsyncCall, _hmm_iwbemservices_cancelasynccall, wbemcli/IWbemServices::CancelAsyncCall, wmi.iwbemservices_cancelasynccall
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
req.dll: Fastprox.dll; Esscli.dll; FrameDyn.dll; FrameDynOS.dll; Ntevt.dll; Stdprov.dll; Viewprov.dll; Wbemcomn.dll; Wbemcore.dll; Wbemess.dll; Wbemsvc.dll; Wmipicmp.dll; Wmidcprv.dll; Wmipjobj.dll; Wmiprvsd.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemServices::CancelAsyncCall
 - wbemcli/IWbemServices::CancelAsyncCall
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fastprox.dll
 - Esscli.dll
 - FrameDyn.dll
 - FrameDynOS.dll
 - Ntevt.dll
 - Stdprov.dll
 - Viewprov.dll
 - Wbemcomn.dll
 - Wbemcore.dll
 - Wbemess.dll
 - Wbemsvc.dll
 - Wmipicmp.dll
 - Wmidcprv.dll
 - Wmipjobj.dll
 - Wmiprvsd.dll
api_name:
 - IWbemServices.CancelAsyncCall
---

# IWbemServices::CancelAsyncCall


## -description

The 
<b>IWbemServices::CancelAsyncCall</b> method cancels any currently pending asynchronous calls based on the 
<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a> pointer, which was  originally passed to the asynchronous method. The outstanding 
<b>IWbemObjectSink</b> pointer can be released prior to the call or after the call returns. The 
<b>CancelAsyncCall</b> method is not operational from within a sink and is not supported by method providers. This means only the client end of the call is canceled. The implementing provider is not notified that the call was canceled and runs to completion. You should consider this before canceling methods that take a long time to complete, such as the <a href="/previous-versions/windows/desktop/vdswmi/defrag-method-in-class-win32-volume">Defrag</a> and <a href="/previous-versions/windows/desktop/vdswmi/format-method-in-class-win32-volume">Format</a> methods in the <a href="/previous-versions/windows/desktop/legacy/aa394515(v=vs.85)">Win32_Volume</a> class.

## -parameters

### -param pSink [in]

Pointer to the 
<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a> implementation provided by the client to any of the asynchronous methods of 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>.

## -returns

This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

On failure, you can obtain available information from the COM function <a href="/windows/desktop/api/oleauto/nf-oleauto-geterrorinfo">GetErrorInfo</a>.

COM-specific error codes can also be returned if network problems cause you to lose the remote connection to Windows Management.

<div class="alert"><b>Note</b>  If 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">SetStatus</a> has not been called on the application's sink by the time WMI processes 
<b>CancelAsyncCall</b>, WMI calls 
<b>SetStatus</b> on that sink with <b>WBEM_E_CALL_CANCELLED</b> as the value for the <i>hResult</i> parameter.</div>
<div> </div>
Timing, and the nature of an asynchronous operation, can affect whether WMI is able to cancel the operation. Only lengthy queries are likely to be successfully canceled before they have completed. Faster operations, such as asynchronous deletions or modifications, typically complete before WMI can process a 
<b>CancelAsyncCall</b> call. So while 
<b>CancelAsyncCall</b> attempts to cancel the current operation, sometimes all that can be done is to release the 
<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a> pointer.

<div class="alert"><b>Note</b>  It is possible to make numerous asynchronous calls using the same object sink. In this case, the 
<b>CancelAsyncCall</b> method cancels all asynchronous calls sharing this object sink. It is strongly recommended that you create one instance of an object sink for each  outstanding asynchronous call.</div>
<div> </div>

## -remarks

Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.  For more information, see <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>. Calling <b>CancelAsyncCall</b> from within an implementation of <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">IWbemObjectSink::Indicate</a> or <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a> can interfere with the WMI state and is not recommended.

In the case of a method call such as <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync">ExecMethodAsync</a>, only the client end of the call is canceled. The implementing provider is not  notified that the call was canceled and  runs to completion.

For more information on how to use asynchronous calls, see <a href="/windows/desktop/WmiSdk/making-an-asynchronous-call-with-c--">Making an Asynchronous Call with C++</a> and <a href="/windows/desktop/WmiSdk/receiving-asynchronous-event-notifications">Receiving Asynchronous Event Notifications</a>



#### Examples

For a full example that uses <b>CancelAsyncCall</b>, see <a href="/windows/desktop/WmiSdk/example--receiving-event-notifications-through-wmi-">Example: Receiving Event Notifications Through WMI</a>


<div class="code"></div>
The following C++ sample, taken from the \\Program Files\Microsoft SDKs\Windows\v7.0\Samples\sysmgmt\wmi\vc\decoupled\instance_provider sample, demonstrates an implementation of <b>CancelAsyncCall</b>.


```cpp
HRESULT CProvider_IWbemServices :: CancelAsyncCall ( 
  
 IWbemObjectSink *a_Sink
)
{
 HRESULT t_Result = WBEM_E_NOT_AVAILABLE ;
 return t_Result ;
}
```

## -see-also

<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>