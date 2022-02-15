---
UID: NF:wbemcli.IWbemCallResult.GetCallStatus
title: IWbemCallResult::GetCallStatus (wbemcli.h)
description: The IWbemCallResult::GetCallStatus method returns to the user the status of the current outstanding semisynchronous call. When this call returns WBEM_S_NO_ERROR, the original call to the IWbemServices method is complete.
helpviewer_keywords: ["GetCallStatus","GetCallStatus method [Windows Management Instrumentation]","GetCallStatus method [Windows Management Instrumentation]","IWbemCallResult interface","IWbemCallResult interface [Windows Management Instrumentation]","GetCallStatus method","IWbemCallResult.GetCallStatus","IWbemCallResult::GetCallStatus","_hmm_iwbemcallresult_getcallstatus","wbemcli/IWbemCallResult::GetCallStatus","wmi.iwbemcallresult_getcallstatus"]
old-location: wmi\iwbemcallresult_getcallstatus.htm
tech.root: wmi
ms.assetid: 5a600fd8-87d8-446d-93da-5b22fd575a11
ms.date: 12/05/2018
ms.keywords: GetCallStatus, GetCallStatus method [Windows Management Instrumentation], GetCallStatus method [Windows Management Instrumentation],IWbemCallResult interface, IWbemCallResult interface [Windows Management Instrumentation],GetCallStatus method, IWbemCallResult.GetCallStatus, IWbemCallResult::GetCallStatus, _hmm_iwbemcallresult_getcallstatus, wbemcli/IWbemCallResult::GetCallStatus, wmi.iwbemcallresult_getcallstatus
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
 - IWbemCallResult::GetCallStatus
 - wbemcli/IWbemCallResult::GetCallStatus
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
 - IWbemCallResult.GetCallStatus
---

# IWbemCallResult::GetCallStatus


## -description

The 
<b>IWbemCallResult::GetCallStatus</b> method returns to the user the status of the current outstanding semisynchronous call. When this call returns <b>WBEM_S_NO_ERROR</b>, the original call to the 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> method is complete.

## -parameters

### -param lTimeout [in]

Specifies the maximum time in milliseconds that this call blocks before it returns. If you use the constant <b>WBEM_INFINITE</b> (0xFFFFFFFF), the call blocks until the original semisynchronous call to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> method is complete. If you use 0 (zero), the call immediately returns the call status.

### -param plStatus [out]

If <b>WBEM_S_NO_ERROR</b> returns in the HRESULT to this method, this parameter will receive the final result status of a call to one of the 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> methods: 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-opennamespace">OpenNamespace</a>, 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstance">PutInstance</a>, 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putclass">PutClass</a>, 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobject">GetObject</a>, 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstance">DeleteInstance</a>, 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-deleteclass">DeleteClass</a>, or 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod">ExecMethod</a>. On error, the value pointed to by <i>plStatus</i> will not be used.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -remarks

On error, you can call the COM function <b>GetErrorInfo</b> to obtain more error information. COM-specific error codes may also be returned if network problems cause you to lose the remote connection to Windows Management.

After invoking an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> method semisynchronously, you can call 
<b>GetCallStatus</b> at any time to determine whether the call is complete. After 
<b>GetCallStatus</b> has returned <b>WBEM_S_NO_ERROR</b>, which indicates completion of the original 
<b>IWbemServices</b> operation, calls to other 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcallresult">IWbemCallResult</a> methods may be required to retrieve the result of the call, according to the following rules:

<ul>
<li>For 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-opennamespace">IWbemServices::OpenNamespace</a>, the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemcallresult-getresultservices">GetResultServices</a> method must be called to retrieve the new 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> pointer.</li>
<li>For 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstance">IWbemServices::PutInstance</a>, the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemcallresult-getresultstring">GetResultString</a> method must be called to obtain the object path that was assigned to the object.</li>
<li>For 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobject">IWbemServices::GetObject</a>, the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemcallresult-getresultobject">GetResultObject</a> method must be called to retrieve the object.</li>
<li>For the 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> methods 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstance">DeleteInstance</a>, 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-deleteclass">DeleteClass</a>, and 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod">ExecMethod</a>, the 
<b>GetCallStatus</b> method is the only call that returns information regarding these operations.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcallresult">IWbemCallResult</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-deleteclass">IWbemServices::DeleteClass</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstance">IWbemServices::DeleteInstance</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod">IWbemServices::ExecMethod</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobject">IWbemServices::GetObject</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-opennamespace">IWbemServices::OpenNamespace</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstance">IWbemServices::PutInstance</a>