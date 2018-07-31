---
UID: NF:wbemcli.IWbemServices.DeleteInstanceAsync
title: IWbemServices::DeleteInstanceAsync
author: windows-sdk-content
description: The IWbemServices::DeleteInstanceAsync method asynchronously deletes an instance of an existing class in the current namespace. The confirmation or failure of the operation is reported through the IWbemObjectSink interface implemented by the caller.
old-location: wmi\iwbemservices_deleteinstanceasync.htm
old-project: WmiSdk
ms.assetid: 7c726842-a274-41d1-b622-681bf9f6ae8b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: DeleteInstanceAsync, DeleteInstanceAsync method [Windows Management Instrumentation], DeleteInstanceAsync method [Windows Management Instrumentation],IWbemServices interface, IWbemServices interface [Windows Management Instrumentation],DeleteInstanceAsync method, IWbemServices.DeleteInstanceAsync, IWbemServices::DeleteInstanceAsync, _hmm_iwbemservices_deleteinstanceasync, wbemcli/IWbemServices::DeleteInstanceAsync, wmi.iwbemservices_deleteinstanceasync
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WMI_OBJ_TEXT
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
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll; Esscli.dll; FrameDyn.dll; FrameDynOS.dll; Ntevt.dll; Stdprov.dll; Viewprov.dll; Wbemcomn.dll; Wbemcore.dll; Wbemess.dll; Wbemsvc.dll; Wmipicmp.dll; Wmidcprv.dll; Wmipjobj.dll; Wmiprvsd.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemServices::DeleteInstanceAsync


## -description


The 
<b>IWbemServices::DeleteInstanceAsync</b> method asynchronously deletes an instance of an existing class in the current namespace. The confirmation or failure of the operation is reported through the 
<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a> interface implemented by the caller.


## -parameters




### -param strObjectPath [in]

Valid <b>BSTR</b> that contains the 
<a href="https://msdn.microsoft.com/78a194f0-cd21-4622-9242-be7e430b96c0">object path</a> of the object to be deleted.


### -param lFlags [in]

<b>WBEM_FLAG_SEND_STATUS</b> registers with Windows Management a request to receive intermediate status reports through the client's implementation of 
<a href="https://msdn.microsoft.com/e47e8cd9-4e80-45c4-b1f0-2f68aea4eb7b">IWbemObjectSink::SetStatus</a>. Provider implementation must support intermediate status reporting, for this flag to change behavior. Note that the <b>WBEM_FLAG_USE_AMENDED_QUALIFIERS</b> flag cannot be used here.


### -param pCtx [in]

Typically <b>NULL</b>. Otherwise, this is a pointer to an 
<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> object that may be used by the provider that is deleting the instance. The values in the context object must be specified in the documentation for the provider in question.


### -param pResponseHandler [in]

Pointer to the caller's implementation of 
<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a>. This handler receives the status of the delete operation as it becomes available through the 
<a href="https://msdn.microsoft.com/e47e8cd9-4e80-45c4-b1f0-2f68aea4eb7b">SetStatus</a> method. If any error code is returned, then the supplied 
<b>IWbemObjectSink</b> pointer is not used. If <b>WBEM_S_NO_ERROR</b> is returned, then the user's 
<b>IWbemObjectSink</b> implementation is called to indicate the result of the operation. Windows Management only calls <a href="_com_iunknown_addref">AddRef</a> on the pointer in cases where <b>WBEM_S_NO_ERROR</b> returns. In cases where an error code returns, the reference count is the same as on entry. For more information, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.


## -returns



This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.

On failure, you can obtain any available information from the COM function <a href=" http://go.microsoft.com/fwlink/p/?linkid=119575">GetErrorInfo</a>.

If 
<b>DeleteInstanceAsync</b> returns <b>WBEM_S_NO_ERROR</b>, WMI waits for a result from the 
<b>SetStatus</b> method of the response handler. WMI waits indefinitely on a local connection, or until a remote connection time-out occurs.

Other error conditions are reported asynchronously to the object sink supplied by the <i>pResponseHandler</i> parameter.

COM-specific error codes also may be returned if network problems cause you to lose the remote connection to Windows Management.

<div class="alert"><b>Note</b>  Clients that call 
<b>DeleteInstanceAsync</b> must always expect the results of the call to be reported using their 
<a href="https://msdn.microsoft.com/96756b27-cbcf-47ce-a8c8-88795a81edde">IWbemObjectSink::Indicate</a> method.</div>
<div> </div>
<div class="alert"><b>Note</b>  When the instance pointed to by <i>strObjectPath</i> belongs to a class that is a member of a class hierarchy, the success of 
<b>DeleteInstanceAsync</b> depends on the topmost non-abstract provider. For a detailed explanation of the dependencies involved that determine the success of this operation, see Remarks in 
<a href="https://msdn.microsoft.com/f6dfeb1d-1730-4df4-adf7-f27dd9edc54d">IWbemServices::DeleteInstance</a>.</div>
<div> </div>



## -remarks



An instance provider can report success or failure with either the return code from 
<b>DeleteInstanceAsync</b> or through a call to 
<b>SetStatus</b> made through <i>pResponseHandler</i>. If sent to 
<b>SetStatus</b>, the return code sent to the sink through <i>pResponseHandler</i> takes precedence. Because the callback might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication. If you require asynchronous communication, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

For more information about using methods semisynchronously, see <a href="https://msdn.microsoft.com/f6dfeb1d-1730-4df4-adf7-f27dd9edc54d">IWbemServices::DeleteInstance</a> and <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.




## -see-also




<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>



<a href="https://msdn.microsoft.com/78a194f0-cd21-4622-9242-be7e430b96c0">Describing an Instance Object Path</a>



<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a>



<a href="https://msdn.microsoft.com/f6dfeb1d-1730-4df4-adf7-f27dd9edc54d">IWbemServices::DeleteInstance</a>
 

 

