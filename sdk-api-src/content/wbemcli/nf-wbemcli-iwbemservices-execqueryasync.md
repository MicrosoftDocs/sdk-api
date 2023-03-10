---
UID: NF:wbemcli.IWbemServices.ExecQueryAsync
title: IWbemServices::ExecQueryAsync (wbemcli.h)
description: The IWbemServices::ExecQueryAsync method executes a query to retrieve objects asynchronously.
helpviewer_keywords: ["ExecQueryAsync","ExecQueryAsync method [Windows Management Instrumentation]","ExecQueryAsync method [Windows Management Instrumentation]","IWbemServices interface","IWbemServices interface [Windows Management Instrumentation]","ExecQueryAsync method","IWbemServices.ExecQueryAsync","IWbemServices::ExecQueryAsync","WBEM_FLAG_BIDIRECTIONAL","WBEM_FLAG_DIRECT_READ","WBEM_FLAG_ENSURE_LOCATABLE","WBEM_FLAG_PROTOTYPE","WBEM_FLAG_SEND_STATUS","WBEM_FLAG_USE_AMENDED_QUALIFIERS","_hmm_iwbemservices_execqueryasync","wbemcli/IWbemServices::ExecQueryAsync","wmi.iwbemservices_execqueryasync"]
old-location: wmi\iwbemservices_execqueryasync.htm
tech.root: wmi
ms.assetid: d8b55500-d84c-431b-93c6-99d1f1b845c3
ms.date: 12/05/2018
ms.keywords: ExecQueryAsync, ExecQueryAsync method [Windows Management Instrumentation], ExecQueryAsync method [Windows Management Instrumentation],IWbemServices interface, IWbemServices interface [Windows Management Instrumentation],ExecQueryAsync method, IWbemServices.ExecQueryAsync, IWbemServices::ExecQueryAsync, WBEM_FLAG_BIDIRECTIONAL, WBEM_FLAG_DIRECT_READ, WBEM_FLAG_ENSURE_LOCATABLE, WBEM_FLAG_PROTOTYPE, WBEM_FLAG_SEND_STATUS, WBEM_FLAG_USE_AMENDED_QUALIFIERS, _hmm_iwbemservices_execqueryasync, wbemcli/IWbemServices::ExecQueryAsync, wmi.iwbemservices_execqueryasync
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
 - IWbemServices::ExecQueryAsync
 - wbemcli/IWbemServices::ExecQueryAsync
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
 - IWbemServices.ExecQueryAsync
---

# IWbemServices::ExecQueryAsync


## -description

The <b>IWbemServices::ExecQueryAsync</b> method executes a query to retrieve objects asynchronously.

## -parameters

### -param strQueryLanguage [in]

Valid <b>BSTR</b> that contains one of the query languages that Windows Management Instrumentation (WMI) supports. This must be "WQL".

### -param strQuery [in]

Valid <b>BSTR</b> that contains the text of the query. This cannot be 
   <b>NULL</b>. When you implement an instance provider, your provider can  refuse the query 
   because it is too complex. When a provider determines that a query is too complex, WMI can retry the provider with 
   a simple  query, or  choose to retrieve and enumerate the superset of the query instances.

For more information on building WMI query strings, see 
   <a href="/windows/desktop/WmiSdk/querying-with-wql">Querying with WQL</a> and the 
   <a href="/windows/desktop/WmiSdk/wql-sql-for-wmi">WQL</a> reference.

### -param lFlags [in]

This parameter can be one of the following values.



#### WBEM_FLAG_USE_AMENDED_QUALIFIERS

If this flag is set, WMI retrieves the amended qualifiers stored in the localized namespace of the current connection's locale. If not set, only the qualifiers stored in the immediate namespace are retrieved.



#### WBEM_FLAG_BIDIRECTIONAL

This flag causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.



#### WBEM_FLAG_SEND_STATUS

This flag registers a request with WMI to receive intermediate status reports through the client's implementation of 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a>. Provider implementation must support intermediate status reporting for this flag to change.



#### WBEM_FLAG_ENSURE_LOCATABLE

This flag ensures that returned objects have enough information in them so that the system properties, such as <b>__PATH</b>, <b>__RELPATH</b>, and <b>__SERVER</b>, are non-<b>NULL</b>.



#### WBEM_FLAG_PROTOTYPE

This flag is used for prototyping. It does not execute the query, but returns an object that looks like a typical result object.



#### WBEM_FLAG_DIRECT_READ

This flag causes direct access to the provider for the class specified without regard to its parent class or subclasses.

### -param pCtx [in]

Typically <b>NULL</b>. Otherwise, this is a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> object that the provider can use to  return the requested classes or instances. The values in the context object must be specified in the documentation for the provider. For more information about this parameter, see 
<a href="/windows/desktop/WmiSdk/making-calls-to-wmi">Making Calls to WMI</a>.

### -param pResponseHandler [in]

Pointer to the caller's implementation of 
<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a>. This handler receives the objects in the query result set as they become available. If any error code is returned, then the supplied 
<b>IWbemObjectSink</b> pointer is not used. If <b>WBEM_S_NO_ERROR</b> is returned, then the user's 
<b>IWbemObjectSink</b> implementation is called to indicate the result of the operation. Windows Management Instrumentation (WMI) calls 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">IWbemObjectSink::Indicate</a> with the objects any number of times, followed by a single call to <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a> to indicate the final status.

WMI only calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> to the pointer when <b>WBEM_S_NO_ERROR</b> returns. When an error code returns, the reference count is the same as on entry. For a detailed explanation of asynchronous calling methods, see 
<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.

## -returns

This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

When there is a  failure, you can obtain   information from the COM function <a href="/windows/win32/api/oleauto/nf-oleauto-geterrorinfo">GetErrorInfo</a>.

Other error codes are returned to the object sink specified by the <i>pResponseHandler</i> parameter.

COM-specific error codes might be returned if network problems cause you to lose the remote connection to WMI.

When finished, an instance provider can report success or failure with either the return code from 
<b>ExecQueryAsync</b> or through a call to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">SetStatus</a> made through <i>pResponseHandler</i>. If you choose to call 
<b>SetStatus</b>, the return code sent through <i>pResponseHandler</i> takes precedence.

## -remarks

There are limits to the number of AND and OR keywords that can be used in WQL queries.  Large numbers of WQL keywords used in a complex query can cause WMI to return the <b>WBEM_E_QUOTA_VIOLATION</b> error code as an <b>HRESULT</b> value.  The limit of WQL keywords depends on how complex the query is.

The caller's <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">IWbemObjectSink::Indicate</a> method can be called to report intermittent status. The <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a> method is called to indicate the end of the result set.

When   a provider does not support query processing, WMI can support it. However, a provider implementation of query processing is probably more efficient than the WMI version. To support queries, your instance provider must implement the 
<b>ExecQueryAsync</b> method. If a provider supports 
<b>ExecQueryAsync</b>, WMI sends a simple unary SELECT query directly to the provider through the <i>strQuery</i> parameter and the provider must parse the query and return the relevant instances. The provider must parse the query because WMI does not modify the query—even when the query is written in WQL.

To use WMI for query processing, do not set the <b>QuerySupportLevels</b> property in your <a href="/windows/desktop/WmiSdk/--instanceproviderregistration">__InstanceProviderRegistration</a>. When you do this, WMI calls your implementation of <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync">CreateInstanceEnumAsync</a> and post filters the results so that the caller only gets those instances that meet the query criteria.

The following example shows a typical instance provider implementation of 
<b>ExecQueryAsync</b>. The 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a> method is called to indicate the end of the result set. It may also be called with no intervening calls to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">IWbemObjectSink::Indicate</a> if error conditions occur.

Because the call-back might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication. If you require asynchronous communication, see <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.

For more information, see <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execquery">IWbemServices::ExecQuery</a> and <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.


```cpp
HRESULT CStdProvider::ExecQueryAsync( 
            /* [in] */ BSTR strQueryLanguage,
            /* [in] */ BSTR strQuery,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [in] */ IWbemObjectSink __RPC_FAR *pResponseHandler
            )
{
   IWbemClassObject *pClass = 0;

// Parse the query.
//   You must implement ParseQuery().
    if (!ParseQuery(strQuery))  return WBEM_E_PROVIDER_NOT_CAPABLE;   

// Assume there is an IWbemServices pointer (m_pSvc) available to 
// retrieve the class definition.
    
    HRESULT hRes = m_pSvc->GetObject(L"ClassName", 0, NULL, &pClass, 0);
    if (FAILED(hRes))
        return hRes;

// Call a method to determine number of instances returned.
// You need to implement the GetNumberInst function.
    int iNumInst = GetNumberInst();

// Now loop through the private source and create each   
// instance which is part of the result set of the query.
    for (int iCnt = 0 ; iCnt < iNumInst ; iCnt++)
    {
// Prepare an empty object to receive the class definition.
         IWbemClassObject *pNextInst = 0;
         hRes = pClass->SpawnInstance(0, &pNextInst);

// Create the instance.
//   You must implement FillInst().
         /*FillInst(pNextInst, iCnt);*/ 

// Deliver the class to WMI.
         pResponseHandler->Indicate(1, &pNextInst);
         pNextInst->Release( );
    }

// Clean up memory
    pClass->Release();
  
// Send finish message to WMI.

    pResponseHandler->SetStatus(0, hRes, 0, 0);

    return hRes;
}
```


In the previous example, the instance provider acquires a thread from WMI to perform the necessary synching operations. You can call the sink <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method and create another thread to deliver the objects in the result set. Creating another thread allows the current thread to return to WMI without depleting the thread pool. Whether the provider chooses the single thread design or the dual thread design depends on how long the provider plans to use the WMI thread. There are no fixed rules. Experimentation can help you determine how your design affects WMI performance.

<div class="alert"><b>Note</b>  When providers implement 
<b>ExecQueryAsync</b>, they are expected by default to return the correct result set based on the query. If a provider cannot return the correct result set easily, it may return a superset of the results and request that WMI do post-filtering before delivering the objects to the client to ensure that the result set is correct. To do this, the provider calls 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">SetStatus</a> on the sink provided to its 
<b>ExecQueryAsync</b> implementation, with the following flags.</div>
<div> </div>

```cpp
// The pSink variable is of type IWbemObjectSink*
pSink->SetStatus(WBEM_STATUS_REQUIREMENTS,
    WBEM_REQUIREMENTS_START_POSTFILTER, 0, 0);
```


<div class="alert"><b>Note</b>  Any objects subsequently sent to the WMI service are filtered. The provider can turn off post-filtering in mid-stream by using the following call.</div>
<div> </div>

```cpp
// The pSink variable is of type IWbemObjectSink*
pSink->SetStatus(WBEM_STATUS_REQUIREMENTS, 
    WBEM_REQUIREMENTS_STOP_POSTFILTER, 0, 0);
```

## -see-also

<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execquery">IWbemServices::ExecQuery</a>



<a href="/windows/desktop/WmiSdk/querying-with-wql">Querying with WQL</a>