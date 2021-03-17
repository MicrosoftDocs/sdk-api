---
UID: NF:wbemglue.CWbemProviderGlue.GetInstancesByQueryAsynch
title: CWbemProviderGlue::GetInstancesByQueryAsynch (wbemglue.h)
description: The GetInstancesByQueryAsynch method retrieves a list of instances supported by a particular provider, and that match a particular query. This method allows the provider to respond asynchronously by returning one instance at a time.
helpviewer_keywords: ["CWbemProviderGlue interface [Windows Management Instrumentation]","GetInstancesByQueryAsynch method","CWbemProviderGlue.GetInstancesByQueryAsynch","CWbemProviderGlue::GetInstancesByQueryAsynch","GetInstancesByQueryAsynch","GetInstancesByQueryAsynch method [Windows Management Instrumentation]","GetInstancesByQueryAsynch method [Windows Management Instrumentation]","CWbemProviderGlue interface","_hmm_cwbemproviderglue_getinstancesbyqueryasynch","wbemglue/CWbemProviderGlue::GetInstancesByQueryAsynch","wmi.cwbemproviderglue_getinstancesbyqueryasynch"]
old-location: wmi\cwbemproviderglue_getinstancesbyqueryasynch.htm
tech.root: wmi
ms.assetid: 51eccecb-5b92-4e06-89eb-552d97074629
ms.date: 12/05/2018
ms.keywords: CWbemProviderGlue interface [Windows Management Instrumentation],GetInstancesByQueryAsynch method, CWbemProviderGlue.GetInstancesByQueryAsynch, CWbemProviderGlue::GetInstancesByQueryAsynch, GetInstancesByQueryAsynch, GetInstancesByQueryAsynch method [Windows Management Instrumentation], GetInstancesByQueryAsynch method [Windows Management Instrumentation],CWbemProviderGlue interface, _hmm_cwbemproviderglue_getinstancesbyqueryasynch, wbemglue/CWbemProviderGlue::GetInstancesByQueryAsynch, wmi.cwbemproviderglue_getinstancesbyqueryasynch
req.header: wbemglue.h
req.include-header: FwCommon.h
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
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CWbemProviderGlue::GetInstancesByQueryAsynch
 - wbemglue/CWbemProviderGlue::GetInstancesByQueryAsynch
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CWbemProviderGlue.GetInstancesByQueryAsynch
---

# CWbemProviderGlue::GetInstancesByQueryAsynch


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/wbemglue/nl-wbemglue-cwbemproviderglue">CWbemProviderGlue</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetInstancesByQueryAsynch</b> method retrieves a list of instances supported by a particular provider, and that match a particular query. This method allows the provider to respond asynchronously by returning one instance at a time.

## -parameters

### -param query

Query to be executed.

### -param pRequester

Pointer of the instance of the class being provided by the framework provider. This "this" pointer is passed to the <i>pCallback</i> function in case the callback function requires it.

### -param pCallback

Pointer to a static function with this prototype.


```cpp
static HRESULT WINAPI Classname::FunctionName(Provider *pProvider,
                                              CInstance *pInstance,
                                              MethodContext *pMethodContext,
                                              void *pUserData );
```


where Classname is the name of a class derived from class <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a>. It is an instance of this class that is the "this" pointer defined by <i>pRequester</i>.

### -param pszNamespace

Namespace for query. If <b>NULL</b>, the default namespace, root\cimv2, is used.

### -param pMethodContext

Pointer to the current context. A context must be provided to prevent deadlocks. Either use the context passed into the provider by <a href="/windows/desktop/api/provider/nf-provider-provider-enumerateinstances">Provider::EnumerateInstances</a> or <a href="/windows/desktop/api/provider/nf-provider-provider-execquery">Provider::ExecQuery</a>, or else obtain it from the instance using <a href="/windows/desktop/api/instance/nf-instance-cinstance-getmethodcontext">CInstance::GetMethodContext</a>. This parameter must not be <b>NULL</b>.

### -param pUserData

Pointer to user-defined data that is passed to the function pointed to by <i>pCallback</i>. If <b>NULL</b>, there is no user-defined data.

## -returns

The method returns <b>WBEM_S_NO_ERROR</b> if the operation was successful, <b>WBEM_E_OUT_OF_MEMORY</b> if the operation failed due to lack of memory, or any other HRESULT error code.

## -remarks

The <b>GetInstancesByQueryAsynch</b> method allows framework providers to access data from other providers without having to make a WMI API call. Framework providers pass a query to <b>GetInstancesByQueryAsynch</b>, which returns the appropriate instances.

For performance reasons, when calling this function, specify only the properties you need (for example, specify SELECT <i>name</i> instead of SELECT *).

Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous communication instead of asynchronous.  If you require asynchronous communication see <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.

For more information about using methods semisynchronously see <a href="/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getinstancesbyquery(lpcwstr_trefpointercollection_cinstance__methodcontext_lpcwstr)">CWbemProviderGlue::GetInstancesByQuery</a> and <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.