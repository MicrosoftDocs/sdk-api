---
UID: NF:wbemcli.IWbemCallResult.GetResultServices
title: IWbemCallResult::GetResultServices (wbemcli.h)
description: Retrieves the IWbemServices pointer, which results from a semisynchronous call to IWbemServices::OpenNamespace when it becomes available.
helpviewer_keywords: ["GetResultServices","GetResultServices method [Windows Management Instrumentation]","GetResultServices method [Windows Management Instrumentation]","IWbemCallResult interface","IWbemCallResult interface [Windows Management Instrumentation]","GetResultServices method","IWbemCallResult.GetResultServices","IWbemCallResult::GetResultServices","_hmm_iwbemcallresult_getresultservices","wbemcli/IWbemCallResult::GetResultServices","wmi.iwbemcallresult_getresultservices"]
old-location: wmi\iwbemcallresult_getresultservices.htm
tech.root: wmi
ms.assetid: 64a4fc4c-f479-4b03-847c-041508e55532
ms.date: 12/05/2018
ms.keywords: GetResultServices, GetResultServices method [Windows Management Instrumentation], GetResultServices method [Windows Management Instrumentation],IWbemCallResult interface, IWbemCallResult interface [Windows Management Instrumentation],GetResultServices method, IWbemCallResult.GetResultServices, IWbemCallResult::GetResultServices, _hmm_iwbemcallresult_getresultservices, wbemcli/IWbemCallResult::GetResultServices, wmi.iwbemcallresult_getresultservices
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
 - IWbemCallResult::GetResultServices
 - wbemcli/IWbemCallResult::GetResultServices
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
 - IWbemCallResult.GetResultServices
---

# IWbemCallResult::GetResultServices


## -description

The 
<b>IWbemCallResult::GetResultServices</b> method  retrieves the 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> pointer, which results from a semisynchronous call to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-opennamespace">IWbemServices::OpenNamespace</a> when it becomes available.

## -parameters

### -param lTimeout [in]

The maximum time in milliseconds that this call blocks before it returns. If you use the constant <b>WBEM_INFINITE</b> (0xFFFFFFFF), the call blocks until the interface pointer is available. If you use 0, the call immediately returns either the pointer or a status code.

### -param ppServices [out]

Cannot be <b>NULL</b>. It receives a pointer to the 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> interface requested by the original call to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-opennamespace">OpenNamespace</a> when it becomes available The caller must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IWbemServices::Release</a> on the returned object when it is no longer required.

On error, a new object is not returned.

## -returns

This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

On error, the COM function <a href="/windows/win32/api/oleauto/nf-oleauto-geterrorinfo">GetErrorInfo</a> can be called to obtain more error information.

COM-specific error codes may also be returned if network problems cause you to lose the remote connection to Windows Management.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcallresult">IWbemCallResult</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-opennamespace">IWbemServices::OpenNamespace</a>