---
UID: NF:wbemglue.CWbemProviderGlue.GetAllInstancesAsynch
title: CWbemProviderGlue::GetAllInstancesAsynch (wbemglue.h)
description: The GetAllInstancesAsynch method retrieves a list of instances returned by a specific class. This method allows the provider to respond asynchronously by returning one instance at a time.
helpviewer_keywords: ["CWbemProviderGlue interface [Windows Management Instrumentation]","GetAllInstancesAsynch method","CWbemProviderGlue.GetAllInstancesAsynch","CWbemProviderGlue::GetAllInstancesAsynch","GetAllInstancesAsynch","GetAllInstancesAsynch method [Windows Management Instrumentation]","GetAllInstancesAsynch method [Windows Management Instrumentation]","CWbemProviderGlue interface","_hmm_cwbemproviderglue_getallinstancesasynch","wbemglue/CWbemProviderGlue::GetAllInstancesAsynch","wmi.cwbemproviderglue_getallinstancesasynch"]
old-location: wmi\cwbemproviderglue_getallinstancesasynch.htm
tech.root: wmi
ms.assetid: 58fe7757-c130-4859-9b60-d08bfb445eb1
ms.date: 12/05/2018
ms.keywords: CWbemProviderGlue interface [Windows Management Instrumentation],GetAllInstancesAsynch method, CWbemProviderGlue.GetAllInstancesAsynch, CWbemProviderGlue::GetAllInstancesAsynch, GetAllInstancesAsynch, GetAllInstancesAsynch method [Windows Management Instrumentation], GetAllInstancesAsynch method [Windows Management Instrumentation],CWbemProviderGlue interface, _hmm_cwbemproviderglue_getallinstancesasynch, wbemglue/CWbemProviderGlue::GetAllInstancesAsynch, wmi.cwbemproviderglue_getallinstancesasynch
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
 - CWbemProviderGlue::GetAllInstancesAsynch
 - wbemglue/CWbemProviderGlue::GetAllInstancesAsynch
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
 - CWbemProviderGlue.GetAllInstancesAsynch
---

# CWbemProviderGlue::GetAllInstancesAsynch


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/wbemglue/nl-wbemglue-cwbemproviderglue">CWbemProviderGlue</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetAllInstancesAsynch</b> method retrieves a list of instances returned by a specific class. This method allows the provider to respond asynchronously by returning one instance at a time.

## -parameters

### -param pszClassName

Name of class for which list of instances should be returned.

### -param pRequester

The "This" pointer for the callback function pointed to by <i>pCallback</i>.

### -param pCallback

Pointer to a static function with this prototype:


```cpp
static HRESULT WINAPI Classname::FunctionName(Provider *pProvider,
                                              CInstance *pInstance,
                                              MethodContext *pMethodContext,
                                              void *pUserData );
```


where Classname is the name of a class derived from class <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a>. It is an instance of this class that is the "this" pointer defined by <i>pRequester</i>. This function is called to return each instance supported by the provider specified by <i>pszClassName</i>.

### -param pszNamespace

Namespace of the provider specified by <i>pszClassName</i>. This parameter can be <b>NULL</b> to indicate the default namespace, which is root\cimv2.

### -param pMethodContext

Pointer to the current context. A context must be provided to prevent deadlocks. Either use the context passed into the provider by <a href="/windows/desktop/api/provider/nf-provider-provider-enumerateinstances">Provider::EnumerateInstances</a> or <a href="/windows/desktop/api/provider/nf-provider-provider-execquery">Provider::ExecQuery</a>, or else obtain it from the instance using <a href="/windows/desktop/api/instance/nf-instance-cinstance-getmethodcontext">CInstance::GetMethodContext</a>. This parameter must not be <b>NULL</b>.

### -param pUserData

Pointer to user-defined data that is passed to the function pointed to by <i>pCallback</i>.

## -returns

The method returns <b>WBEM_S_NO_ERROR</b> if the operation was successful, <b>WBEM_E_OUT_OF_MEMORY</b> if the operation failed due to lack of memory, or any other HRESULT error code.

## -remarks

The <b>GetAllInstancesAsynch</b> method performs almost the same function as <a href="/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances">GetAllInstances</a>. However, instead of returning one arbitrarily large array of instances, the provider passes an instance to the function specified by <i>pCallback</i> each time the instance is retrieved from a provider. This allows the provider to use less memory, and to begin returning instances to the client sooner.

<div class="alert"><b>Note</b>  Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.  For more information, see <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.</div>
<div> </div>
This method is semantically equivalent to the query SELECT * FROM <i>pszBaseClassName</i> WHERE<b> __</b>Class = <i>pszBaseClassName</i>.