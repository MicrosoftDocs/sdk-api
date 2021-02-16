---
UID: NF:wbemcli.IWbemServices.PutInstanceAsync
title: IWbemServices::PutInstanceAsync (wbemcli.h)
description: The IWbemServices::PutInstanceAsync method asynchronously creates or updates an instance of an existing class. Update confirmation or error reporting is provided through the IWbemObjectSink interface implemented by the caller.
helpviewer_keywords: ["IWbemServices interface [Windows Management Instrumentation]","PutInstanceAsync method","IWbemServices.PutInstanceAsync","IWbemServices::PutInstanceAsync","PutInstanceAsync","PutInstanceAsync method [Windows Management Instrumentation]","PutInstanceAsync method [Windows Management Instrumentation]","IWbemServices interface","WBEM_FLAG_CREATE_ONLY","WBEM_FLAG_CREATE_OR_UPDATE","WBEM_FLAG_SEND_STATUS","WBEM_FLAG_UPDATE_ONLY","WBEM_FLAG_USE_AMENDED_QUALIFIERS","_hmm_iwbemservices_putinstanceasync","wbemcli/IWbemServices::PutInstanceAsync","wmi.iwbemservices_putinstanceasync"]
old-location: wmi\iwbemservices_putinstanceasync.htm
tech.root: wmi
ms.assetid: fef3eb72-74ba-49cd-b992-292405d29917
ms.date: 12/05/2018
ms.keywords: IWbemServices interface [Windows Management Instrumentation],PutInstanceAsync method, IWbemServices.PutInstanceAsync, IWbemServices::PutInstanceAsync, PutInstanceAsync, PutInstanceAsync method [Windows Management Instrumentation], PutInstanceAsync method [Windows Management Instrumentation],IWbemServices interface, WBEM_FLAG_CREATE_ONLY, WBEM_FLAG_CREATE_OR_UPDATE, WBEM_FLAG_SEND_STATUS, WBEM_FLAG_UPDATE_ONLY, WBEM_FLAG_USE_AMENDED_QUALIFIERS, _hmm_iwbemservices_putinstanceasync, wbemcli/IWbemServices::PutInstanceAsync, wmi.iwbemservices_putinstanceasync
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
 - IWbemServices::PutInstanceAsync
 - wbemcli/IWbemServices::PutInstanceAsync
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
 - IWbemServices.PutInstanceAsync
---

# IWbemServices::PutInstanceAsync


## -description

The <b>IWbemServices::PutInstanceAsync</b> 
   method asynchronously creates or updates an instance of an existing class. Update confirmation or error reporting 
   is provided through the <a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a> interface 
   implemented by the caller.

## -parameters

### -param pInst [in]

Pointer to the instance to be written to the WMI repository. The caller cannot make assumptions about the 
    reference count at the completion of this call.

### -param lFlags [in]

Specifies whether the caller wants the instance created if the instance does not currently exist.

When implementing an instance provider, you can choose to support a limited number of the flags in 
       <i>lFlags</i> by returning <b>WBEM_E_PROVIDER_NOT_CAPABLE</b>.


This property can have one or more of the following values.





#### WBEM_FLAG_CREATE_OR_UPDATE

This flag causes this instance to be created if it does not exist or be overwritten if it exists already.



#### WBEM_FLAG_UPDATE_ONLY

Updates an existing instance.



#### WBEM_FLAG_CREATE_ONLY

This flag is for instance creation only. The call fails if the class already exists.



#### WBEM_FLAG_SEND_STATUS

This flag registers with Windows Management a request to receive intermediate status reports through the 
        clients implementation of 
        <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a>. Provider 
        implementation must support intermediate status reporting for this flag to change behavior.



#### WBEM_FLAG_USE_AMENDED_QUALIFIERS

If this flag is set, WMI does not store any qualifiers with the 
        <b>Amended</b> flavor. If this flag is not set, it is assumed that this object is 
        not localized, and all qualifiers are stored with this instance.

### -param pCtx [in]

Pointer describing if the client is requesting a partial-instance update or full-instance update. A partial-instance update modifies a subset of the properties of the instance. In contrast, a full-instance update modifies all of the properties. If <b>NULL</b>, this parameter indicates that the caller application is requesting a full-instance update. Otherwise, this is a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> object required by the dynamic class provider that is producing the class instances. For more information about this parameter, see 
<a href="/windows/desktop/WmiSdk/making-calls-to-wmi">Making Calls to WMI</a>.

### -param pResponseHandler [in]

Pointer to the caller's implementation of 
<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a>. This handler receives the status of this call when it becomes available using the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a> method. If any error code is returned, then the supplied 
<b>IWbemObjectSink</b> pointer is not used. If <b>WBEM_S_NO_ERROR</b> is returned, then the user's 
<b>IWbemObjectSink</b> implementation is called to indicate the result of the operation. Windows Management only calls <b>AddRef</b> on the pointer in cases where <b>WBEM_S_NO_ERROR</b> returns. In cases where an error code returns, the reference count is the same as on entry. For more information about how to make asynchronous calls, see 
<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

Note that if 
<b>PutInstanceAsync</b> returns <b>WBEM_S_NO_ERROR</b>, WMI waits for a result from the 
<b>SetStatus</b> method of the response handler. WMI waits indefinitely on a local connection or until a remote connection time-out occurs.

COM-specific error codes also may be returned if network problems cause you to lose the remote connection to Windows Management.

## -remarks

Clients that call 
<b>PutInstanceAsync</b> must always expect the results of the call to be reported using their 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">IWbemObjectSink::Indicate</a> method.

When the instance pointed to by <i>pInst</i> belongs to a class that is derived from other classes, the success of 
<b>PutInstanceAsync</b> depends on the success of the providers responsible for the parent classes. For example, if <i>pInst</i> belongs to <b>ClassB</b> and <b>ClassB</b> derives from <b>ClassA</b>, a call to the 
<b>PutInstanceAsync</b> method implemented by the provider for <b>ClassA</b> must succeed for the update operation on <b>ClassB</b> to succeed. For more information, see Remarks in 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstance">IWbemServices::PutInstance</a>.

When implementing an instance provider, if the instance has a key property set to <b>NULL</b>, 
<b>PutInstanceAsync</b> should choose a value guaranteed to be unique within the class. When WMI services a request to update an instance with a <b>NULL</b> key property, it internally generates a <b>GUID</b> and assigns it to the key property. Further, when the instance being updated belongs to a child class, the success of the operation is dependent on the success of a 
<b>PutInstanceAsync</b> call to each of the providers responsible for the classes higher in the hierarchy. Do not return <b>WBEM_S_NO_ERROR</b> until you are sure that all of the other providers have succeeded. For more information, see 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstance">IWbemServices::PutInstance</a>.

Instance providers supporting a partial update must check for the existence of the <b>__PUT_EXTENSIONS</b> context value. A system context value is a value defined by WMI to have specific meanings, is set by the client application, and is supported by an instance provider. The 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> interface provides access to the system context values and other provider-specific context values. The following list lists the context values that support partial-instance update operations.

The 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a> method is called to indicate the end of the result set. It may also be called with no intervening calls to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">IWbemObjectSink::Indicate</a> if error conditions occur.

Because the call-back might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication. If you require asynchronous communication, see <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.

For more information about using methods semisynchronously, see <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstance">IWbemServices::PutInstance</a> and <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.

<table>
<tr>
<th>System context value</th>
<th>Description</th>
</tr>
<tr>
<td>
<b>__PUT_EXTENSIONS</b>

(<b>VT_BOOL</b>)

</td>
<td>
The client application has set one or more of the other system context values to provide more information about the update operation.

</td>
</tr>
<tr>
<td>
<b>__PUT_EXT_STRICT_NULLS</b>

(<b>VT_BOOL</b>)

</td>
<td>
The instance provider must force the setting of properties to <b>VT_NULL</b> when appropriate and raise an error on failure.

</td>
</tr>
<tr>
<td>
<b>__PUT_EXT_PROPERTIES</b>

(<b>VT_ARRAY</b> | <b>VT_BSTR</b>)

</td>
<td>
Contains a list of the properties to update. The instance provider should ignore all other properties.

</td>
</tr>
<tr>
<td>
<b>__PUT_EXT_ATOMIC</b>

(<b>VT_BOOL</b>)

</td>
<td>
All updates must succeed or the instance provider must revert back. There can be no partial success.

</td>
</tr>
</table>
 

When implementing an instance provider, you should respond to a <b>NULL</b> property in <i>pCtx</i> in the following manner:

<ul>
<li>If the property type is <b>VT_NULL</b>, the provider can either ignore the property without making a change or fail the operation.</li>
<li>If the property type is not <b>VT_NULL</b> and the property cannot be updated, the provider should return an error, because the provider is obligated to update the property with the new value.</li>
</ul>
If <i>pCtx</i> is not <b>NULL</b> and points to valid context information, the caller application is requesting a partial-instance update. As before, an instance providers that does not support partial-instance updating should fail the operation by returning <b>WBEM_E_PROVIDER_NOT_CAPABLE</b>.

When implementing an async operation, the async operation not complete until you release any <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a>'s you have performed on <i>pResponseHandler</i>.  This is the case even if you call <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">SetStatus</a> on <i>pResponseHander</i>. If <i>pResponseHandler</i> is leaked, any sync or semi-sync clients will also not complete and possibly stop responding, depending on your implementation.

Even in catastrophic cases, you must release the references for decoupled providers. This is because in sync and semi-sync cases, the WMI service owns the implementation of <i>pResponseHandler</i>: even if your decoupled provider's process exits, the clients will still not be responding.


#### Examples

The following example describes how to structure 
     <b>PutInstanceAsync</b>.


```cpp
HRESULT CStdProvider::PutInstanceAsync( 
            /* [in] */ IWbemClassObject __RPC_FAR *pInst,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [in] */ IWbemObjectSink __RPC_FAR *pResponseHandler
            )
{
   // You must implement the InstanceIsValid method
   // to check to see if the instance in the pInst variable
   // is valid.
   if (InstanceIsValid(lFlags, pInst)) 
   {
       return WBEM_S_NO_ERROR;
   }

   return WBEM_E_PROVIDER_NOT_CAPABLE;   
}
```

## -see-also

<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>



<a href="/windows/desktop/WmiSdk/creating-an-instance">Creating an Instance</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>