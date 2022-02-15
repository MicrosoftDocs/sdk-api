---
UID: NF:wbemcli.IEnumWbemClassObject.NextAsync
title: IEnumWbemClassObject::NextAsync (wbemcli.h)
description: Use the NextAsync method when a controlled asynchronous retrieval of objects to a sink is required.
helpviewer_keywords: ["IEnumWbemClassObject interface [Windows Management Instrumentation]","NextAsync method","IEnumWbemClassObject.NextAsync","IEnumWbemClassObject::NextAsync","NextAsync","NextAsync method [Windows Management Instrumentation]","NextAsync method [Windows Management Instrumentation]","IEnumWbemClassObject interface","_hmm_ienumwbemclassobject_nextasync","wbemcli/IEnumWbemClassObject::NextAsync","wmi.ienumwbemclassobject_nextasync"]
old-location: wmi\ienumwbemclassobject_nextasync.htm
tech.root: wmi
ms.assetid: 1ff82982-a2d7-4618-8488-9e4b7628012d
ms.date: 12/05/2018
ms.keywords: IEnumWbemClassObject interface [Windows Management Instrumentation],NextAsync method, IEnumWbemClassObject.NextAsync, IEnumWbemClassObject::NextAsync, NextAsync, NextAsync method [Windows Management Instrumentation], NextAsync method [Windows Management Instrumentation],IEnumWbemClassObject interface, _hmm_ienumwbemclassobject_nextasync, wbemcli/IEnumWbemClassObject::NextAsync, wmi.ienumwbemclassobject_nextasync
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
 - IEnumWbemClassObject::NextAsync
 - wbemcli/IEnumWbemClassObject::NextAsync
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
 - IEnumWbemClassObject.NextAsync
---

# IEnumWbemClassObject::NextAsync


## -description

Use the <b>NextAsync</b> method when a controlled asynchronous retrieval of objects to a sink is required. Normal asynchronous retrieval, such as a call to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync">IWbemServices::ExecQueryAsync</a>, results in uncontrolled delivery of objects to the caller's implementation of 
<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a>. This method is helpful for cases where a component controls object delivery.

## -parameters

### -param uCount [in]

Number of objects being requested.

### -param pSink [in]

Sink to receive the objects. The sink must be implemented by the caller. As each batch of objects is requested, they are delivered to the <i>pSink</i> parameter of the 
      <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">Indicate</a> method followed by a final call to the <i>pSink</i> parameter of the <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">SetStatus</a> method. If the sink is going to be used to deliver objects, this method returns <b>WBEM_S_NO_ERROR</b>, even if the number of objects to be delivered is less than requested. However, if there are no more objects remaining, then the <i>pSink</i> parameter is ignored (no calls to the <i>pSink</i> parameter of <b>SetStatus</b> are made). Instead, this method returns <b>WBEM_S_FALSE</b>.

## -returns

The 
<b>NextAsync</b> method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -remarks

A call to the COM function <a href="/windows/win32/api/oleauto/nf-oleauto-geterrorinfo">GetErrorInfo</a> provides more information about the error. COM-specific error codes may also be returned if network problems cause you to lose the remote connection to Windows Management.

This call returns immediately and delivery to the sink occurs in the background. If multiple calls are made to this method from one or more threads, they are logically queued and the order of calls and object delivery is preserved. Multiple calls made to this method from one or more threads block do not return until all the sink objects related to previous calls to this method have been serviced. A call to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-ienumwbemclassobject-reset">Reset</a> does not affect delivery of objects currently in progress as a result of previous calls. The 
<b>Reset</b> method only causes new calls to start at the beginning of the object sequence.

If the number of requested objects is immediately available, the function returns <b>WBEM_S_NO_ERROR</b>. If less than the number of requested objects are available, the available objects are returned and <b>WBEM_S_NO_ERROR</b> are returned. The remainder of the objects are delivered by the user-supplied sink.

As the objects become available, the caller's implementation of 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">IWbemObjectSink::Indicate</a> is called zero or more times to deliver the objects. This is followed by a call to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a> with a value of <b>WBEM_S_NO_ERROR</b> if <i>uCount</i> items are returned.

If fewer objects are available than the number requested, <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">Indicate</a> is called for those objects that are available. <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">SetStatus</a> is then called with a value of <b>WBEM_S_FALSE</b>, or the error code if an error occurred.

If the requested number of objects is delivered, the final object is followed by a call to <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">SetStatus</a> with a status code of <b>WBEM_S_NO_ERROR</b>. If the enumeration completes before the requested number of objects can be delivered, the <b>SetStatus</b> method has a status code of <b>WBEM_S_FALSE</b>.

If there are no available objects, <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">Indicate</a> is not called. However, a final call to <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">SetStatus</a> always occurs to indicate the status of the entire operation.

Because the callback might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication. If you require asynchronous communication, see <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.

For more information about using methods semisynchronously, see <a href="/windows/desktop/api/wbemcli/nf-wbemcli-ienumwbemclassobject-next">IEnumWbemClassObject::Next</a> and <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.