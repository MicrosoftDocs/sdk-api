---
UID: NF:wbemcli.IWbemServices.PutClassAsync
title: IWbemServices::PutClassAsync (wbemcli.h)
description: The IWbemServices::PutClassAsync method creates a new class, or updates an existing one.
helpviewer_keywords: ["IWbemServices interface [Windows Management Instrumentation]","PutClassAsync method","IWbemServices.PutClassAsync","IWbemServices::PutClassAsync","PutClassAsync","PutClassAsync method [Windows Management Instrumentation]","PutClassAsync method [Windows Management Instrumentation]","IWbemServices interface","WBEM_FLAG_CREATE_ONLY","WBEM_FLAG_CREATE_OR_UPDATE","WBEM_FLAG_OWNER_UPDATE","WBEM_FLAG_SEND_STATUS","WBEM_FLAG_UPDATE_COMPATIBLE","WBEM_FLAG_UPDATE_FORCE_MODE","WBEM_FLAG_UPDATE_ONLY","WBEM_FLAG_UPDATE_SAFE_MODE","WBEM_FLAG_USE_AMENDED_QUALIFIERS","_hmm_iwbemservices_putclassasync","wbemcli/IWbemServices::PutClassAsync","wmi.iwbemservices_putclassasync"]
old-location: wmi\iwbemservices_putclassasync.htm
tech.root: wmi
ms.assetid: 957f5646-86e7-4632-9012-b1fb281b65fb
ms.date: 12/05/2018
ms.keywords: IWbemServices interface [Windows Management Instrumentation],PutClassAsync method, IWbemServices.PutClassAsync, IWbemServices::PutClassAsync, PutClassAsync, PutClassAsync method [Windows Management Instrumentation], PutClassAsync method [Windows Management Instrumentation],IWbemServices interface, WBEM_FLAG_CREATE_ONLY, WBEM_FLAG_CREATE_OR_UPDATE, WBEM_FLAG_OWNER_UPDATE, WBEM_FLAG_SEND_STATUS, WBEM_FLAG_UPDATE_COMPATIBLE, WBEM_FLAG_UPDATE_FORCE_MODE, WBEM_FLAG_UPDATE_ONLY, WBEM_FLAG_UPDATE_SAFE_MODE, WBEM_FLAG_USE_AMENDED_QUALIFIERS, _hmm_iwbemservices_putclassasync, wbemcli/IWbemServices::PutClassAsync, wmi.iwbemservices_putclassasync
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
 - IWbemServices::PutClassAsync
 - wbemcli/IWbemServices::PutClassAsync
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
 - IWbemServices.PutClassAsync
---

# IWbemServices::PutClassAsync


## -description

The <b>IWbemServices::PutClassAsync</b> method 
    creates a new class, or updates an existing one. The class specified by the <i>pObject</i> 
    parameter must be correctly initialized with all of the required property values. The call immediately returns. 
    Success or failure is supplied to the object sink specified by the <i>pResponseHandler</i> 
    parameter.

## -parameters

### -param pObject [in]

Pointer to the object containing the class definition.

### -param lFlags [in]

One or more of the following values are valid.



#### WBEM_FLAG_USE_AMENDED_QUALIFIERS

If this flag is set, WMI does not store any qualifiers with the <b>amended</b> flavor. If this flag is not set, it is assumed that this object is not localized, and all qualifiers are stored with this instance.



#### WBEM_FLAG_CREATE_OR_UPDATE

This flag causes this class to be created if it does not exist or be overwritten if it exists already.



#### WBEM_FLAG_UPDATE_ONLY

Updates an existing class.



#### WBEM_FLAG_CREATE_ONLY

This flag is for class creation only. The call fails if the class already exists.



#### WBEM_FLAG_SEND_STATUS

This flag registers with Windows Management a request to receive intermediate status reports through the client's implementation of 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a>. Provider implementation must support intermediate status reporting for this flag to change behavior.



#### WBEM_FLAG_OWNER_UPDATE

Push providers must specify this flag when calling 
<b>PutClassAsync</b> to indicate that this class has changed.



#### WBEM_FLAG_UPDATE_COMPATIBLE

This flag allows a class to be updated if there are no derived classes and there are no instances for that class. It also allows updates in all cases if the change is just to non-important qualifiers (for example, the <b>Description</b> qualifier). This is the default behavior for this call and is used for compatibility with previous versions of Windows Management. If the class has instances or changes are to important qualifiers, the update fails.



#### WBEM_FLAG_UPDATE_SAFE_MODE

This flag allows updates of classes even if there are child classes, as long as the change does not cause any conflicts with child classes. An example of an update this flag would allow would be to add a new property to the base class that was not previously mentioned in any of the child classes. If the class has instances, the update fails.



#### WBEM_FLAG_UPDATE_FORCE_MODE

This flag forces updates of classes when conflicting child classes exist. An example of an update this flag would force would be if a class qualifier were defined in a child class, and the base class tried to add the same qualifier which conflicted with the existing one. In force mode, this conflict would be resolved by deleting the conflicting qualifier in the child class.

### -param pCtx [in]

Typically <b>NULL</b>. Otherwise, this is a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> object that may be used by the provider that is receiving the requested class. The values in the context object must be specified in the documentation for the provider in question. For more information about this parameter, see 
<a href="/windows/desktop/WmiSdk/making-calls-to-wmi">Making Calls to WMI</a>.

### -param pResponseHandler [in]

Pointer to the caller's implementation of 
<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a>. This handler receives the status of the 
<b>Put</b> request when the status becomes available using the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">SetStatus</a> method. If any error code is returned, then the supplied 
<b>IWbemObjectSink</b> pointer is not used. If <b>WBEM_S_NO_ERROR</b> is returned, then the user's 
<b>IWbemObjectSink</b> implementation is called to indicate the result of the operation. Windows Management only calls <b>AddRef</b> to the pointer in cases where <b>WBEM_S_NO_ERROR</b> returns. In cases where an error code returns, the reference count is the same as on entry. For a detailed explanation of this parameter, see 
<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

Other status or error codes are reported to the object sink specified by the <i>pReponseHandler</i> parameter.

COM-specific error codes also may be returned if network problems cause you to lose the remote connection to Windows Management.

Note that if 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync">PutInstanceAsync</a> returns <b>WBEM_S_NO_ERROR</b>, WMI waits for a result from the 
<b>SetStatus</b> method of the response handler. WMI waits indefinitely on a local connection or until a remote connection time-out occurs.

Because returning <b>WBEM_E_FAILED</b> causes other providers to not have a chance to create the class, it should only be returned when the class provider has failed in a way that might later succeed.

<div class="alert"><b>Note</b>  Unpredictable behavior will result if you change class definitions while they are in use by clients or providers. The 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putclass">IWbemServices::PutClass</a> method should only be used to create or update a class when there are no clients or providers currently using the class.</div>
<div> </div>

## -remarks

If multiple class providers are installed for one particular class, WMI will not recognize which class 
    provider is capable of creating that class.

The <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a> method is 
    called to indicate the end of the result set. It may also be called with no intervening calls to 
    <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">IWbemObjectSink::Indicate</a> if error conditions 
    occur.

Because the call-back might not be returned at the same authentication level as the client requires, it is 
     recommended that you use semisynchronous instead of asynchronous communication. If you require asynchronous 
     communication, see <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.

For more information about using methods semisynchronously, see 
     <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putclass">IWbemServices::PutClass</a> and 
     <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.


#### Examples

The following code example describes a simple implementation of 
<b>PutClassAsync</b>.


```cpp
HRESULT CStdProvider::PutClassAsync( 
            /* [in] */ IWbemClassObject __RPC_FAR *pObject,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [in] */ IWbemObjectSink __RPC_FAR *pResponseHandler
            )
{
    // You must implement the ClassIsValid function yourself to
    // determine if the class contains a valid instance
   if (ClassIsValid(lFlags, pObject))
   {
       return WBEM_S_NO_ERROR;
   }

   return WBEM_E_PROVIDER_NOT_CAPABLE;   
}
```

## -see-also

<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>



<a href="/windows/desktop/WmiSdk/creating-a-class">Creating a Class</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putclass">IWbemServices::PutClass</a>