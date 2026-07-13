---
UID: NF:wbemcli.IWbemCallResult.GetResultString
title: IWbemCallResult::GetResultString (wbemcli.h)
description: The IWbemCallResult::GetResultString method returns the assigned object path of an instance newly created by IWbemServices::PutInstance.
helpviewer_keywords: ["GetResultString","GetResultString method [Windows Management Instrumentation]","GetResultString method [Windows Management Instrumentation]","IWbemCallResult interface","IWbemCallResult interface [Windows Management Instrumentation]","GetResultString method","IWbemCallResult.GetResultString","IWbemCallResult::GetResultString","_hmm_iwbemcallresult_getresultstring","wbemcli/IWbemCallResult::GetResultString","wmi.iwbemcallresult_getresultstring"]
old-location: wmi\iwbemcallresult_getresultstring.htm
tech.root: wmi
ms.assetid: 7a022519-c112-42d4-b777-c3828439f7dd
ms.date: 12/05/2018
ms.keywords: GetResultString, GetResultString method [Windows Management Instrumentation], GetResultString method [Windows Management Instrumentation],IWbemCallResult interface, IWbemCallResult interface [Windows Management Instrumentation],GetResultString method, IWbemCallResult.GetResultString, IWbemCallResult::GetResultString, _hmm_iwbemcallresult_getresultstring, wbemcli/IWbemCallResult::GetResultString, wmi.iwbemcallresult_getresultstring
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
 - IWbemCallResult::GetResultString
 - wbemcli/IWbemCallResult::GetResultString
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
 - IWbemCallResult.GetResultString
---

# IWbemCallResult::GetResultString


## -description

The 
<b>IWbemCallResult::GetResultString</b> method returns the assigned object path of an instance newly created by 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstance">IWbemServices::PutInstance</a>.
<div class="alert"><b>Note</b>  The call result object is primarily used when the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstance">PutInstance</a> call is carried out by a provider and the client needs to know the object path (the values of the key properties) assigned the provider. For example, if the class key property is a globally unique identifier (GUID), assigned by the provider during the 
<b>PutInstance</b> operation, the client would have no way of knowing this GUID unless the provider was able to return it in this way.</div><div> </div>

## -parameters

### -param lTimeout [in]

Specifies the maximum time in milliseconds that this call blocks before returning. If you use the constant <b>WBEM_INFINITE</b> (0xFFFFFFFF), the call blocks until the object path is available. If you use 0, the call immediately returns either the object path or a status code.

### -param pstrResultString [out]

Cannot be <b>NULL</b>. This parameter receives a pointer to the object path, which, in turn, leads to the newly created object. The returned string must be deallocated using the system call <i>SysFreeString</i>. On error, a new string is not returned.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

On error, you can call the COM function <b>GetErrorInfo</b> to obtain more error information.

COM-specific error codes may also be returned if network problems cause you to lose the remote connection to Windows Management.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcallresult">IWbemCallResult</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstance">IWbemServices::PutInstance</a>