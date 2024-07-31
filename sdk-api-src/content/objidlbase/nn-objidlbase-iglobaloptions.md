---
UID: NN:objidlbase.IGlobalOptions
title: IGlobalOptions (objidlbase.h)
description: The IGlobalOptions (objidlbase.h) interface sets and queries global properties of the Component Object Model (COM) runtime.
helpviewer_keywords: ["IGlobalOptions","IGlobalOptions interface [COM]","IGlobalOptions interface [COM]","described","_com_iglobaloptions","com.iglobaloptions","objidlbase/IGlobalOptions"]
old-location: com\iglobaloptions.htm
tech.root: com
ms.assetid: c5e823be-521d-4eb4-8836-fdd2cac6f15d
ms.date: 08/15/2022
ms.keywords: IGlobalOptions, IGlobalOptions interface [COM], IGlobalOptions interface [COM],described, _com_iglobaloptions, com.iglobaloptions, objidlbase/IGlobalOptions
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - IGlobalOptions
 - objidlbase/IGlobalOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IGlobalOptions
---

# IGlobalOptions interface


## -description

Sets and queries global properties of the Component Object Model (COM) runtime.

## -inheritance

The <b>IGlobalOptions</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGlobalOptions</b> also has these types of members:

## -remarks

The following global properties of the COM runtime can be set and queried with this interface.

<table>
<tr>
<th>Property</th>
<th>Values</th>
</tr>
<tr>
<td>
COMGLB_APPID

</td>
<td>
The AppID for the process.
This is the only supported property on Windows XP.

</td>
</tr>
<tr>
<td>
COMGLB_EXCEPTION_HANDLING

</td>
<td>
Possible values for the COMGLB_EXCEPTION_HANDLING property are:



<ul>
<li>COMGLB_EXCEPTION_HANDLE: This is the default behavior. This setting causes the COM runtime to handle fatal exceptions.
</li>
<li>COMGLB_EXCEPTION_DONOT_HANDLE: This causes the COM runtime not to handle fatal exceptions.</li>
<li>COMGLB_EXCEPTION_DONOT_HANDLE_FATAL: Alias for COMGLB_EXCEPTION_DONOT_HANDLE. Supported in Windows 7 and later.</li>
<li>COMGLB_EXCEPTION_DONOT_HANDLE_ANY: When set and a fatal exception occurs in a COM method, this causes the COM runtime to not handle the exception.

When set and a non-fatal exception occurs in a COM method, this causes the COM runtime to create a Windows Error Reporting (WER) dump and terminate the process.
Supported in Windows 7 and later.</li>
</ul>
By default, the COM runtime handles fatal exceptions raised during method invocations by returning the RPC_E_SERVERFAULT error code to the client. An application disables this behavior to allow exceptions to propagate to WER, which creates application process dumps and terminates the application. This prevents possible data corruption and allows an application vendor to debug the dumps.

<div class="alert"><b>Note</b>  Even if COM runtime exception handling is disabled, exceptions might not propagate to WER if there is another application-level exception handler in the process that handles the exception.</div>
<div> </div>
For new applications, it is recommended that the COMGLB_EXCEPTION_HANDLING property be set to COMGLB_EXCEPTION_DONOT_HANDLE_ANY.

</td>
</tr>
<tr>
<td>
COMGLB_RPC_THREADPOOL_SETTING  

</td>
<td>
Possible values for the COMGLB_RPC_THREADPOOL_SETTING property in the <a href="/windows/desktop/api/objidl/nf-objidl-iglobaloptions-set">Set</a> method are:



<ul>
<li>COMGLB_RPC_THREADPOOL_SETTING_PRIVATE_POOL: Instructs RPC to use a dedicated private thread pool.
</li>
</ul>
Possible values for the COMGLB_RPC_THREADPOOL_SETTING property in the <a href="/windows/desktop/api/objidl/nf-objidl-iglobaloptions-query">Query</a> method are:



<ul>
<li>COMGLB_RPC_THREADPOOL_SETTING_PRIVATE_POOL: RPC uses a dedicated private thread pool.
</li>
<li>COMGLB_RPC_THREADPOOL_SETTING_DEFAULT_POOL: RPC uses the system default thread pool.</li>
</ul>
RPC uses the system thread pool by default in Windows 7. Since the system thread pool is shared by multiple components in the process, COM and RPC operations may behave incorrectly if the thread pool state is corrupted by a component.

The COMGLB_RPC_THREADPOOL_SETTING property can be used to change the RPC thread pool behavior. Changing the default behavior will incur a performance penalty since this causes RPC to use an extra thread. Therefore, care should be exercised when changing this setting. It is recommended that this setting is changed only for application compatibility reasons.

<div class="alert"><b>Note</b>  This property must be set immediately after COM is initialized in the process. If this property is set after performing any operations that cause COM to initialize the RPC channel (for example, marshaling or unmarshalling object references), the <a href="/windows/desktop/api/objidl/nf-objidl-iglobaloptions-set">Set</a> method will fail.</div>
<div> </div>
<b>Note</b>  This property is only supported in Windows 7 and later versions of Windows.

</td>
</tr>
<tr>
<td>
COMGLB_RO_SETTINGS

</td>
<td>
Possible values for the COMGLB_RO_SETTINGS property are:



<ul>
<li>COMGLB_FAST_RUNDOWN: Indicates that stubs in the current process are subjected to fast stub  rundown behavior, which means that stubs are run down on termination of the client process, instead of waiting for normal cleanup timeouts to expire. </li>
<li>COMGLB_STA_MODALLOOP_REMOVE_TOUCH_MESSAGES: Remove touch messages from the message queue in the STA modal loop.
</li>
<li>COMGLB_STA_MODALLOOP_SHARED_QUEUE_REMOVE_INPUT_MESSAGES: Input messages are removed in
   the STA modal loop when the thread's message queue is attached.</li>
<li>COMGLB_STA_MODALLOOP_SHARED_QUEUE_DONOT_REMOVE_INPUT_MESSAGES: Input messages aren't removed in
   the STA modal loop when the thread's message queue is attached.</li>
<li>COMGLB_STA_MODALLOOP_SHARED_QUEUE_REORDER_POINTER_MESSAGES: Pointer input messages aren't removed in the STA modal loop when the thread's message queue is attached but are temporarily masked to avoid deadlocks arising from the attached queue.
</li>
<li>COMGLB_RESERVED1: Reserved for future use.</li>
<li>COMGLB_RESERVED2: Reserved for future use.</li>
<li>COMGLB_RESERVED3: Reserved for future use.</li>
</ul>
<b>Note</b>  This property is only supported in Windows 8 and later versions of Windows.

</td>
</tr>
<tr>
<td>
COMGLB_UNMARSHALING_POLICY

</td>
<td>
Possible values for the COMGLB_UNMARSHALING_POLICY property are:



<ul>
<li>COMGLB_UNMARSHALING_POLICY_NORMAL: Unmarshaling behavior is the same as versions before than Windows 8. <b>EOAC_NO_CUSTOM_MARSHAL</b> restrictions apply if this flag is set in <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a>. Otherwise, there are no restrictions. This is the default for processes that aren't in the app container.</li>
<li>COMGLB_UNMARSHALING_POLICY_STRONG: Unmarshaling allows only a system-trusted list of hardened unmarshalers and unmarshalers allowed per-process by the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coallowunmarshalerclsid">CoAllowUnmarshalerCLSID</a> function. This is the default for processes in the app container.</li>
<li> COMGLB_UNMARSHALING_POLICY_HYBRID: Unmarshaling data whose source is app container allows only a system-trusted list of hardened unmarshalers and unmarshalers allowed per-process by the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coallowunmarshalerclsid">CoAllowUnmarshalerCLSID</a> function. Unmarshaling behavior for data with a source that's not app container is unchanged from previous versions.</li>
</ul>
<b>Note</b>  This property is only supported in Windows 8 and later versions of Windows.

</td>
</tr>
</table>
 

It's important for applications that detect crashes and other exceptions that might be generated while executing inbound COM calls, for example a call on a local server or when executing the <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop">IDropTarget::Drop</a> method, to set COMGLB_EXCEPTION_HANDLING to COMGLB_EXCEPTION_DONOT_HANDLE to disable COM behavior of catching exceptions.  Failure to do this can lead to corrupt process state, for example locks held when these exceptions are thrown are abandoned, and the process could enter an inconsistent state.

All such applications should execute this code at startup.


``` syntax
    IGlobalOptions *pGlobalOptions;
    hr =  CoCreateInstance(CLSID_GlobalOptions, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pGlobalOptions));
    if (SUCCEEDED(hr))
    {
        hr = pGlobalOptions->Set(COMGLB_EXCEPTION_HANDLING, COMGLB_EXCEPTION_DONOT_HANDLE);
        pGlobalOptions->Release();
    }

```


## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imarshalingstream">IMarshalingStream</a>
