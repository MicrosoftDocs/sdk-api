---
UID: NF:wbemcli.IWbemServices.DeleteInstanceAsync
title: IWbemServices::DeleteInstanceAsync (wbemcli.h)
description: The IWbemServices::DeleteInstanceAsync method asynchronously deletes an instance of an existing class in the current namespace. The confirmation or failure of the operation is reported through the IWbemObjectSink interface implemented by the caller.
helpviewer_keywords: ["DeleteInstanceAsync","DeleteInstanceAsync method [Windows Management Instrumentation]","DeleteInstanceAsync method [Windows Management Instrumentation]","IWbemServices interface","IWbemServices interface [Windows Management Instrumentation]","DeleteInstanceAsync method","IWbemServices.DeleteInstanceAsync","IWbemServices::DeleteInstanceAsync","_hmm_iwbemservices_deleteinstanceasync","wbemcli/IWbemServices::DeleteInstanceAsync","wmi.iwbemservices_deleteinstanceasync"]
old-location: wmi\iwbemservices_deleteinstanceasync.htm
tech.root: wmi
ms.assetid: 7c726842-a274-41d1-b622-681bf9f6ae8b
ms.date: 12/05/2018
ms.keywords: DeleteInstanceAsync, DeleteInstanceAsync method [Windows Management Instrumentation], DeleteInstanceAsync method [Windows Management Instrumentation],IWbemServices interface, IWbemServices interface [Windows Management Instrumentation],DeleteInstanceAsync method, IWbemServices.DeleteInstanceAsync, IWbemServices::DeleteInstanceAsync, _hmm_iwbemservices_deleteinstanceasync, wbemcli/IWbemServices::DeleteInstanceAsync, wmi.iwbemservices_deleteinstanceasync
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
 - IWbemServices::DeleteInstanceAsync
 - wbemcli/IWbemServices::DeleteInstanceAsync
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
 - IWbemServices.DeleteInstanceAsync
---

# IWbemServices::DeleteInstanceAsync


## -description

The 
<b>IWbemServices::DeleteInstanceAsync</b> method asynchronously deletes an instance of an existing class in the current namespace. The confirmation or failure of the operation is reported through the 
<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a> interface implemented by the caller.

## -parameters

### -param strObjectPath [in]

Valid <b>BSTR</b> that contains the 
<a href="/windows/desktop/WmiSdk/describing-an-instance-object-path">object path</a> of the object to be deleted.

### -param lFlags [in]

<b>WBEM_FLAG_SEND_STATUS</b> registers with Windows Management a request to receive intermediate status reports through the client's implementation of 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a>. Provider implementation must support intermediate status reporting, for this flag to change behavior. Note that the <b>WBEM_FLAG_USE_AMENDED_QUALIFIERS</b> flag cannot be used here.

### -param pCtx [in]

Typically <b>NULL</b>. Otherwise, this is a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> object that may be used by the provider that is deleting the instance. The values in the context object must be specified in the documentation for the provider in question.

### -param pResponseHandler [in]

Pointer to the caller's implementation of 
<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a>. This handler receives the status of the delete operation as it becomes available through the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">SetStatus</a> method. If any error code is returned, then the supplied 
<b>IWbemObjectSink</b> pointer is not used. If <b>WBEM_S_NO_ERROR</b> is returned, then the user's 
<b>IWbemObjectSink</b> implementation is called to indicate the result of the operation. Windows Management only calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the pointer in cases where <b>WBEM_S_NO_ERROR</b> returns. In cases where an error code returns, the reference count is the same as on entry. For more information, see 
<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.

## -returns

This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

On failure, you can obtain any available information from the COM function <a href="/windows/win32/api/oleauto/nf-oleauto-geterrorinfo">GetErrorInfo</a>.

If 
<b>DeleteInstanceAsync</b> returns <b>WBEM_S_NO_ERROR</b>, WMI waits for a result from the 
<b>SetStatus</b> method of the response handler. WMI waits indefinitely on a local connection, or until a remote connection time-out occurs.

Other error conditions are reported asynchronously to the object sink supplied by the <i>pResponseHandler</i> parameter.

COM-specific error codes also may be returned if network problems cause you to lose the remote connection to Windows Management.

<div class="alert"><b>Note</b>  Clients that call 
<b>DeleteInstanceAsync</b> must always expect the results of the call to be reported using their 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">IWbemObjectSink::Indicate</a> method.</div>
<div> </div>
<div class="alert"><b>Note</b>  When the instance pointed to by <i>strObjectPath</i> belongs to a class that is a member of a class hierarchy, the success of 
<b>DeleteInstanceAsync</b> depends on the topmost non-abstract provider. For a detailed explanation of the dependencies involved that determine the success of this operation, see Remarks in 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstance">IWbemServices::DeleteInstance</a>.</div>
<div> </div>

## -remarks

An instance provider can report success or failure with either the return code from 
<b>DeleteInstanceAsync</b> or through a call to 
<b>SetStatus</b> made through <i>pResponseHandler</i>. If sent to 
<b>SetStatus</b>, the return code sent to the sink through <i>pResponseHandler</i> takes precedence. Because the callback might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication. If you require asynchronous communication, see <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.

For more information about using methods semisynchronously, see <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstance">IWbemServices::DeleteInstance</a> and <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.

## -see-also

<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>



<a href="/windows/desktop/WmiSdk/describing-an-instance-object-path">Describing an Instance Object Path</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstance">IWbemServices::DeleteInstance</a>