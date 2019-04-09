---
UID: NF:wbemglue.CWbemProviderGlue.GetAllDerivedInstancesAsynch
title: CWbemProviderGlue::GetAllDerivedInstancesAsynch (wbemglue.h)
author: windows-sdk-content
description: The GetAllDerivedInstancesAsynch method retrieves a list of instances supported by a particular provider and derived from a particular base class. This method allows the provider to respond asynchronously by returning one instance at a time.
old-location: wmi\cwbemproviderglue_getallderivedinstancesasynch.htm
tech.root: WmiSdk
ms.assetid: d58f8aca-2176-443e-b82a-87ee8bae8cf8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CWbemProviderGlue interface [Windows Management Instrumentation],GetAllDerivedInstancesAsynch method, CWbemProviderGlue.GetAllDerivedInstancesAsynch, CWbemProviderGlue::GetAllDerivedInstancesAsynch, GetAllDerivedInstancesAsynch, GetAllDerivedInstancesAsynch method [Windows Management Instrumentation], GetAllDerivedInstancesAsynch method [Windows Management Instrumentation],CWbemProviderGlue interface, _hmm_cwbemproviderglue_getallderivedinstancesasynch, wbemglue/CWbemProviderGlue::GetAllDerivedInstancesAsynch, wmi.cwbemproviderglue_getallderivedinstancesasynch
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CWbemProviderGlue.GetAllDerivedInstancesAsynch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CWbemProviderGlue::GetAllDerivedInstancesAsynch


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/493027c2-e54d-4fad-9e33-98d1ceab8860">CWbemProviderGlue</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetAllDerivedInstancesAsynch</b> method retrieves a list of instances supported by a particular provider and derived from a particular base class. This method allows the provider to respond asynchronously by returning one instance at a time.


## -parameters




### -param pszBaseClassName

Name of base class for which the list should be returned.


### -param pRequester

Pointer for the callback function pointed to by <i>pCallback</i>.


### -param pCallback

Pointer to a <b>static</b> function with this prototype.


```cpp
  static HRESULT WINAPI Classname::FunctionName(
     Provider *pProvider,
     CInstance *pInstance,
     MethodContext *pMethodContext,
     void *pUserData );
```


where Classname is the name of a class derived from class <a href="https://msdn.microsoft.com/d8a7c433-7e6a-45cc-914f-a15a3688c7aa">Provider</a>. It is an instance of this class that is the "this" pointer defined by <i>pRequester</i>. This function is called to return each instance supported by the provider specified by <i>pszClassName</i>.


### -param pszNamespace

Namespace of the class name specified by <i>pszClassName</i>. When this parameter is <b>NULL</b>, the default namespace root\cimv2 is used.


### -param pMethodContext

Pointer to the current context. A context must be provided to prevent deadlocks. Either use the context passed into the provider by <a href="https://msdn.microsoft.com/9566acb0-d7bf-4d3d-b7da-5cfbce150a2c">Provider::EnumerateInstances</a> or <a href="https://msdn.microsoft.com/94d5c8ee-2d61-42af-9a22-cc0df423b245">Provider::ExecQuery</a>, or else obtain it from the instance using <a href="https://msdn.microsoft.com/a2033754-4fd0-405f-9ad9-737eb8931016">CInstance::GetMethodContext</a>. This parameter must not be <b>NULL</b>.


### -param pUserData

Pointer to user-defined data that is passed to the function pointed to by <i>pCallback</i>.


## -returns



The method returns <b>WBEM_S_NO_ERROR</b> if the operation was successful, <b>WBEM_E_OUT_OF_MEMORY</b> if the operation failed due to lack of memory, or any other HRESULT error code.




## -remarks



The <b>GetAllDerivedInstancesAsynch</b> method performs almost the same function as <a href="https://msdn.microsoft.com/ecdca316-12a0-46c3-97df-85a087533837">GetAllDerivedInstances</a>. However, instead of returning one arbitrarily large array of instances, the provider passes an instance to the function specified by <i>pCallBack</i> each time the instance is retrieved from a provider. This allows the provider to use less memory, and to begin returning instances to the client sooner.

This method is semantically equivalent to the query SELECT * FROM <i>pszBaseClassName</i>.

Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous communication instead of asynchronous.  If, however,  you require asynchronous communication, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

For more information about using methods semisynchronously,  see <a href="https://msdn.microsoft.com/ecdca316-12a0-46c3-97df-85a087533837">CWbemProviderGlue::GetAllDerivedInstances</a> and <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.



