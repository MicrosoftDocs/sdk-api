---
UID: NF:wbemcli.IWbemServices.DeleteClassAsync
title: IWbemServices::DeleteClassAsync (wbemcli.h)
description: The IWbemServices::DeleteClassAsync method deletes the specified class from the current namespace.
helpviewer_keywords: ["DeleteClassAsync","DeleteClassAsync method [Windows Management Instrumentation]","DeleteClassAsync method [Windows Management Instrumentation]","IWbemServices interface","IWbemServices interface [Windows Management Instrumentation]","DeleteClassAsync method","IWbemServices.DeleteClassAsync","IWbemServices::DeleteClassAsync","WBEM_FLAG_OWNER_UPDATE","WBEM_FLAG_SEND_STATUS","_hmm_iwbemservices_deleteclassasync","wbemcli/IWbemServices::DeleteClassAsync","wmi.iwbemservices_deleteclassasync"]
old-location: wmi\iwbemservices_deleteclassasync.htm
tech.root: wmi
ms.assetid: ebb58f3b-201c-4e37-8a51-9b5e2365cf3c
ms.date: 12/05/2018
ms.keywords: DeleteClassAsync, DeleteClassAsync method [Windows Management Instrumentation], DeleteClassAsync method [Windows Management Instrumentation],IWbemServices interface, IWbemServices interface [Windows Management Instrumentation],DeleteClassAsync method, IWbemServices.DeleteClassAsync, IWbemServices::DeleteClassAsync, WBEM_FLAG_OWNER_UPDATE, WBEM_FLAG_SEND_STATUS, _hmm_iwbemservices_deleteclassasync, wbemcli/IWbemServices::DeleteClassAsync, wmi.iwbemservices_deleteclassasync
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
 - IWbemServices::DeleteClassAsync
 - wbemcli/IWbemServices::DeleteClassAsync
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
 - IWbemServices.DeleteClassAsync
---

# IWbemServices::DeleteClassAsync


## -description

The 
<b>IWbemServices::DeleteClassAsync</b> method deletes the specified class from the current namespace. This method is identical to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-deleteclass">IWbemServices::DeleteClass</a> except that the call returns immediately. Confirmation or failure is asynchronously reported to the specified object sink using the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a> method after the operation is complete.

## -parameters

### -param strClass [in]

Name of the class targeted for deletion.

### -param lFlags [in]

One or more of the following values are valid.



#### WBEM_FLAG_SEND_STATUS

This flag registers with Windows Management a request to receive intermediate status reports through the client's implementation of 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a>. Provider implementation must support intermediate status reporting, for this flag to change behavior.



#### WBEM_FLAG_OWNER_UPDATE

Push providers must specify this flag when calling 
<b>DeleteClassAsync</b> to indicate that this class has changed.

### -param pCtx [in]

Typically <b>NULL</b>. Otherwise, this is a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> object that may be used by the provider deleting the class. The values in the context object must be specified in the documentation for the provider in question. For more information about this parameter, see 
<a href="/windows/desktop/WmiSdk/making-calls-to-wmi">Making Calls to WMI</a>.

### -param pResponseHandler [in]

Pointer to an implementation of 
<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a> implemented by the caller. This handler receives the status of the deletion request when it becomes available through the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a> method. If any error code is returned, then the supplied 
<b>IWbemObjectSink</b> pointer is not used. If <b>WBEM_S_NO_ERROR</b> is returned, then the user's 
<b>IWbemObjectSink</b> implementation is called to indicate the result of the operation. Windows Management only calls <b>AddRef</b> on the pointer in cases where <b>WBEM_S_NO_ERROR</b> returns. In cases where an error code returns, the reference count is the same as on entry. For a detailed explanation of this parameter, see 
<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

All other return codes are provided to the object sink specified by the <i>pReponseHandler</i> parameter through the 
<b>SetStatus</b> method. Error conditions, such as when the class does not exist or the user does not have permission to delete classes, are reported to the handler. They are not reported in the return code of this method.

COM-specific error codes also may be returned if network problems cause you to lose the remote connection to Windows Management.

## -remarks

If a dynamic instance provider is associated with the class, the provider is unregistered, and is no longer called for that class. Any classes that derive from the deleted class are also deleted, and their associated providers become unregistered. All outstanding static instances of the specified class and its subclasses are also deleted when the class is deleted.

If the class is provided by a dynamic class provider, the success of the deletion depends on whether class deletion is supported by that provider.

<div class="alert"><b>Note</b>  Standard system classes cannot be deleted.</div>
<div> </div>
Because the call-back might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication. If you require asynchronous communication, see <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.

For more information about using methods semisynchronously, see <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-deleteclass">IWbemServices::DeleteClass</a> and <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-deleteclass">IWbemServices::DeleteClass</a>



<a href="/windows/desktop/WmiSdk/retrieving-an-error-code">Retrieving an Error Code</a>