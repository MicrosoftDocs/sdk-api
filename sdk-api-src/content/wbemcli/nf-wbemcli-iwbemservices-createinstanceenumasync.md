---
UID: NF:wbemcli.IWbemServices.CreateInstanceEnumAsync
title: IWbemServices::CreateInstanceEnumAsync (wbemcli.h)
description: The IWbemServices::CreateInstanceEnumAsync method creates an enumerator that asynchronously returns the instances of a specified class according to user-specified selection criteria.
helpviewer_keywords: ["CreateInstanceEnumAsync","CreateInstanceEnumAsync method [Windows Management Instrumentation]","CreateInstanceEnumAsync method [Windows Management Instrumentation]","IWbemServices interface","IWbemServices interface [Windows Management Instrumentation]","CreateInstanceEnumAsync method","IWbemServices.CreateInstanceEnumAsync","IWbemServices::CreateInstanceEnumAsync","WBEM_FLAG_BIDIRECTIONAL","WBEM_FLAG_DEEP","WBEM_FLAG_DIRECT_READ","WBEM_FLAG_SEND_STATUS","WBEM_FLAG_SHALLOW","WBEM_FLAG_USE_AMENDED_QUALIFIERS","_hmm_iwbemservices_createinstanceenumasync","wbemcli/IWbemServices::CreateInstanceEnumAsync","wmi.iwbemservices_createinstanceenumasync"]
old-location: wmi\iwbemservices_createinstanceenumasync.htm
tech.root: wmi
ms.assetid: 5ba2ff28-034f-4949-9bde-8c98345ec7c6
ms.date: 12/05/2018
ms.keywords: CreateInstanceEnumAsync, CreateInstanceEnumAsync method [Windows Management Instrumentation], CreateInstanceEnumAsync method [Windows Management Instrumentation],IWbemServices interface, IWbemServices interface [Windows Management Instrumentation],CreateInstanceEnumAsync method, IWbemServices.CreateInstanceEnumAsync, IWbemServices::CreateInstanceEnumAsync, WBEM_FLAG_BIDIRECTIONAL, WBEM_FLAG_DEEP, WBEM_FLAG_DIRECT_READ, WBEM_FLAG_SEND_STATUS, WBEM_FLAG_SHALLOW, WBEM_FLAG_USE_AMENDED_QUALIFIERS, _hmm_iwbemservices_createinstanceenumasync, wbemcli/IWbemServices::CreateInstanceEnumAsync, wmi.iwbemservices_createinstanceenumasync
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
 - IWbemServices::CreateInstanceEnumAsync
 - wbemcli/IWbemServices::CreateInstanceEnumAsync
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
 - IWbemServices.CreateInstanceEnumAsync
---

# IWbemServices::CreateInstanceEnumAsync


## -description

The 
<b>IWbemServices::CreateInstanceEnumAsync</b> method creates an enumerator that asynchronously returns the instances of a specified class according to user-specified selection criteria. This method supports simple WMI Query Language (WQL) queries. More complex queries can be processed using the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync">IWbemServices::ExecQueryAsync</a> method.

## -parameters

### -param strFilter [in]

Valid <b>BSTR</b> containing the name of the class for which instances are desired. This parameter cannot be <b>NULL</b>.

### -param lFlags [in]

This parameter can be one of the following values.



#### WBEM_FLAG_USE_AMENDED_QUALIFIERS

If this flag is set, Windows Management Instrumentation (WMI) retrieves the amended qualifiers stored in the localized namespace of the current connection's locale. If not set, only the qualifiers stored in the immediate namespace are retrieved.



#### WBEM_FLAG_DEEP

This flag forces the enumeration to include instances of this and all subclasses in the hierarchy.



#### WBEM_FLAG_SHALLOW

This flag forces the enumeration to include only pure instances of this class, excluding all instances of subclasses, which supply properties not found in this class.



#### WBEM_FLAG_SEND_STATUS

This flag registers with Windows Management a request to receive intermediate status reports through the clients implementation of 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a>. Provider implementation must support intermediate status reporting for this flag to change behavior.



#### WBEM_FLAG_BIDIRECTIONAL

This flag causes Windows Management to retain pointers to objects of the enumeration until the client releases the enumerator.



#### WBEM_FLAG_DIRECT_READ

This flag causes direct access to the provider for the class specified without any regard to its parent class or subclasses.

### -param pCtx [in]

Typically NULL. Otherwise, this is a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> object that may be used by the provider that is returning the requested instances. The values in the context object must be specified in the documentation for the provider in question. For more information, see 
<a href="/windows/desktop/WmiSdk/making-calls-to-wmi">Making Calls to WMI</a>.

### -param pResponseHandler [in]

Pointer to the caller's implementation of 
<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a>. This handler receives the objects as they become available. If any error code is returned, then the supplied 
<b>IWbemObjectSink</b> pointer is not used. If <b>WBEM_S_NO_ERROR</b> is returned, then the user's 
<b>IWbemObjectSink</b> implementation will be called to indicate the result of the operation. Windows Management only calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the pointer in cases where <b>WBEM_S_NO_ERROR</b> returns. In cases where an error code returns, the reference count is the same as on entry. For more information, see 
<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

On failure, you can obtain more information from the COM function <a href="/windows/desktop/api/oleauto/nf-oleauto-geterrorinfo">GetErrorInfo</a>.

COM-specific error codes also may be returned if network problems cause you to lose the remote connection to Windows Management.

An instance provider can report success or failure with either the return code from 
<b>CreateInstanceEnumAsync</b>, or through a call to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">SetStatus</a> made through <i>pResponseHandler</i>. If you choose to call 
<b>SetStatus</b>, the return code sent through <i>pResponseHandler</i> takes precedence.

If 
<b>CreateInstanceEnumAsync</b> returns <b>WBEM_S_NO_ERROR</b>, WMI waits for a result from the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">SetStatus</a> method of the response handler. WMI waits indefinitely on a local connection, or until a remote connection time-out occurs.

## -remarks

The 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a> method is called to indicate the end of the result set. It may also be called with no intervening calls to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">IWbemObjectSink::Indicate</a> if error conditions occur.

Because the callback might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.

For more information, see <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum">IWbemServices::CreateInstanceEnum</a> and <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.


#### Examples

The following example shows you how to implement 
<b>CreateInstanceEnumAsync</b>.


```cpp
#define NUM_OF_INSTANCES 3

HRESULT CStdProvider::CreateInstanceEnumAsync( 
            /* [in] */ BSTR strClass,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [in] */ IWbemObjectSink __RPC_FAR *pResponseHandler
            )
{
    IWbemClassObject *pClass = 0; 
    IWbemClassObject *pNextInst = 0;

    // Assume there is an IWbemServices pointer available to
    // retrieve the class definition.
    HRESULT hRes = m_pSvc->GetObject(strClass, 0, NULL, &pClass, 0);
    if (hRes)
        return hRes;

    // Now loop through the private source and create each instance.
    for (int i = 0; i < NUM_OF_INSTANCES; i++)
    {
         // Prepare an empty object to receive the class definition.
         pClass->SpawnInstance(0, &pNextInst);

         // Create the instance.
         // For example, create the instance in a
         // FillInst method you implement:
         /*FillInst(pNextInst);*/

         // Deliver the class to WMI.
         pResponseHandler->Indicate(1, &pNextInst);
         pNextInst->Release();
    }

    // Send a finish message to WMI.
    pResponseHandler->SetStatus(0, WBEM_S_NO_ERROR, 0, 0);

    // Free memory resources.
    SysFreeString(strClass);
    pClass->Release();
    m_pSvc->Release();

    return WBEM_S_NO_ERROR;
}
```


In the previous example, the instance provider acquires a thread from WMI to perform any necessary operations. You may want to call the sink <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method and create another thread for delivering the objects in the result set. Creating another thread allows the current thread to return to WMI without depleting the thread pool. Whether or not  the provider chooses the single thread design over the dual thread design depends on how long the provider plans to use the WMI thread. There are no fixed rules. Experimentation can help you determine how your design affects WMI performance.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum">IWbemServices::CreateInstanceEnum</a>