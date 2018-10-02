---
UID: NF:combaseapi.CoDisconnectContext
title: CoDisconnectContext function
author: windows-sdk-content
description: Disconnects all proxy connections that are being maintained on behalf of all interface pointers that point to objects in the current context.
old-location: com\codisconnectcontext.htm
tech.root: com
ms.assetid: faacb583-285a-4ec6-9700-22320e87de6e
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: CoDisconnectContext, CoDisconnectContext function [COM], _com_CoDisconnectContext, com.codisconnectcontext, combaseapi/CoDisconnectContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoDisconnectContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CoDisconnectContext function


## -description


Disconnects all proxy connections that are being maintained on behalf of all interface pointers that point to objects in the current context.

This function blocks connections until all objects are successfully disconnected or the time-out expires. Only the context that actually manages the objects should call <b>CoDisconnectContext</b>.


## -parameters




### -param dwTimeout [in]

The time in milliseconds after which <b>CoDisconnectContext</b> returns even if the proxy connections for all objects have not been disconnected. INFINITE is an acceptable value for this parameter.



## -returns



This function can return the standard return values E_FAIL, E_INVALIDARG, and E_OUTOFMEMORY, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The proxy connections for all objects were successfully disconnected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
Not all proxy connections were successfully deleted in the time specified in <i>dwTimeout</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The current context cannot be disconnected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONTEXT_E_WOULD_DEADLOCK</b></dt>
</dl>
</td>
<td width="60%">
An object tried to call <a href="https://msdn.microsoft.com/faacb583-285a-4ec6-9700-22320e87de6e">CoDisconnectContext</a> on the context it is residing in. This would cause the function to time-out and deadlock if <i>dwTimeout</i> were set to INFINITE.


</td>
</tr>
</table>
 




## -remarks



The <b>CoDisconnectContext</b> function is used to support unloading services in shared service hosts where you must unload your service's binaries without affecting other COM servers that are running in the same process. If you control the process lifetime and you do not unload until the process exits, the COM infrastructure will perform the necessary cleanup automatically and you do not have to call this function.

The <b>CoDisconnectContext</b> function enables a server to correctly disconnect all external clients of all objects in the current context. Default contexts cannot be disconnected. To use <b>CoDisconnectContext</b>, you must first create a context that can be disconnected and register your class factories for objects from which you want to disconnect within that context. You can do this with the <a href="https://msdn.microsoft.com/47af7b80-3419-4a40-8932-a5a27f297dc9">IContextCallback</a> interface.



If <b>CoDisconnectContext</b> returns RPC_E_TIMEOUT, this does not indicate that the function did not disconnect the objects, but that not all disconnections could be completed in the time specified by <i>dwTimeout</i> because of outstanding calls on the objects. All objects will be disconnected after all calls on them have been completed.



It is not safe to unload the DLL that hosts the service until <b>CoDisconnectContext</b> returns S_OK. If the function returns RPC_E_TIMEOUT, the service may perform other clean-up. The service must call the function until it returns S_OK, and then it can safely unload its DLL.



The <b>CoDisconnectContext</b> function performs the following tasks:

<ul>
<li>Calls <a href="https://msdn.microsoft.com/4293316a-bafe-4fca-ad6a-68d8e99c8fba">CoDisconnectObject</a> on all objects in the current context.</li>
<li>Blocks until all objects have been disconnected or the time-out has expired.</li>
</ul>
The <b>CoDisconnectContext</b> function has the following limitations:

<ul>
<li>Asynchronous COM calls are not supported.</li>
<li>In-process objects must be registered and enabled using the CLSCTX_LOCAL_SERVER flag, or they will not be disconnected.
</li>
<li>COM+ is not supported.</li>
<li>COM interface pointers are context-sensitive. Therefore, any interface pointer created in the context to be disconnected can only be used within that context.</li>
</ul>

#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IContextCallback *icc;
hr = CoCreateInstance(CLSID_ContextSwitcher, NULL, CLSCTX_INPROC_SERVER, IID_IContextCallback, (void**)&amp;icc);

icc-&gt;ContextCallback(EnterCallback, NULL, IID_IContextCallback, 5, NULL);

HRESULT __stdcall EnterCallback(ComCallData *pv)
{ 
    return CoRegisterClassObject(...);
}

/* All objects created by the class factories registered in the callback will be put into the newly created context.
To disconnect, re-enter the context, revoke the class factories, and call CoDisconnectContext. */

icc-&gt;ContextCallback(DisconnectCallback, NULL, IID_IContextCallback, 5, NULL);

HRESULT __stdcall DisconnectCallback(ComCallData *pv)
{
    CoRevokeClassObject(...);
    return CoDisconnectContext(timeout);
}

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/4293316a-bafe-4fca-ad6a-68d8e99c8fba">CoDisconnectObject</a>



<a href="https://msdn.microsoft.com/47af7b80-3419-4a40-8932-a5a27f297dc9">IContextCallback</a>
 

 

