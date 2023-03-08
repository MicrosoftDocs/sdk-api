---
UID: NF:wbemcli.IWbemCallResult.GetResultObject
title: IWbemCallResult::GetResultObject (wbemcli.h)
description: The IWbemCallResult::GetResultObject method attempts to retrieve an object from a previous semisynchronous call to IWbemServices::GetObject or IWbemServices::ExecMethod.
helpviewer_keywords: ["GetResultObject","GetResultObject method [Windows Management Instrumentation]","GetResultObject method [Windows Management Instrumentation]","IWbemCallResult interface","IWbemCallResult interface [Windows Management Instrumentation]","GetResultObject method","IWbemCallResult.GetResultObject","IWbemCallResult::GetResultObject","_hmm_iwbemcallresult_getresultobject","wbemcli/IWbemCallResult::GetResultObject","wmi.iwbemcallresult_getresultobject"]
old-location: wmi\iwbemcallresult_getresultobject.htm
tech.root: wmi
ms.assetid: 06603f26-587f-4aff-8ae3-7f77f9b266f5
ms.date: 12/05/2018
ms.keywords: GetResultObject, GetResultObject method [Windows Management Instrumentation], GetResultObject method [Windows Management Instrumentation],IWbemCallResult interface, IWbemCallResult interface [Windows Management Instrumentation],GetResultObject method, IWbemCallResult.GetResultObject, IWbemCallResult::GetResultObject, _hmm_iwbemcallresult_getresultobject, wbemcli/IWbemCallResult::GetResultObject, wmi.iwbemcallresult_getresultobject
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemCallResult::GetResultObject
 - wbemcli/IWbemCallResult::GetResultObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemcli.h
api_name:
 - IWbemCallResult.GetResultObject
---

# IWbemCallResult::GetResultObject


## -description

The 
<b>IWbemCallResult::GetResultObject</b> method attempts to retrieve an object from a previous semisynchronous call to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobject">IWbemServices::GetObject</a> or 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod">IWbemServices::ExecMethod</a>. If the object is not yet available, the call returns <b>WBEM_S_TIMEDOUT</b>. Also, before invoking this method to get the resulting object, you may call 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus">IWbemCallResult::GetCallStatus</a> until it returns <b>WBEM_S_NO_ERROR</b>, indicating that the original semisynchronous operation is complete.

## -parameters

### -param lTimeout [in]

Specifies the maximum time in milliseconds that this call blocks before returning. If you use the constant <b>WBEM_INFINITE</b> (0xFFFFFFFF), the call blocks until the object is available. If you use 0, the call immediately returns either the object or a status code.

### -param ppResultObject [out]

This parameter cannot be <b>NULL</b>. It receives the copy of the object when it becomes available. You must call <b>IWbemClassObject::Release</b> on the returned object when the object is no longer required. A new object is not returned on error.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

If the original semisynchronous operation failed (such as when the object was not found, or the method could not be invoked), this method returns the error code that the original function would have returned in its synchronous version.

On error, you can call the COM function <b>GetErrorInfo</b> to obtain more error information.

COM-specific error codes may also be returned if network problems cause you to lose the remote connection to Windows Management.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcallresult">IWbemCallResult</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod">IWbemServices::ExecMethod</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobject">IWbemServices::GetObject</a>