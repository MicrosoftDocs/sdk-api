---
UID: NF:wbemprov.IWbemProviderInit.Initialize
title: IWbemProviderInit::Initialize
author: windows-sdk-content
description: Called by Windows Management to initialize a provider to receive client requests. All types of providers must implement this method.
old-location: wmi\iwbemproviderinit_initialize.htm
tech.root: WmiSdk
ms.assetid: 437d803d-b916-4209-bbf0-64b1ec3b7068
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWbemProviderInit interface [Windows Management Instrumentation],Initialize method, IWbemProviderInit.Initialize, IWbemProviderInit::Initialize, Initialize, Initialize method [Windows Management Instrumentation], Initialize method [Windows Management Instrumentation],IWbemProviderInit interface, _hmm_iwbemproviderinit_initialize, wbemprov/IWbemProviderInit::Initialize, wmi.iwbemproviderinit_initialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wbemprov.h
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
req.dll: Wbemsvc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemsvc.dll
api_name:
 - IWbemProviderInit.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemProviderInit::Initialize


## -description


The 
<b>IWbemProviderInit::Initialize</b> method is called by Windows Management to initialize a provider to receive client requests. All types of providers must implement this method.


## -parameters




### -param wszUser [in]

A pointer to the user name, if per-user initialization was requested in the 
<a href="https://msdn.microsoft.com/41e0d938-00c6-4f4c-8027-8b8512398dee">__Win32Provider</a> registration instance for this provider. Otherwise, this is <b>NULL</b>.

Be aware that this parameter is set to <b>NULL</b> for event consumer providers regardless of the value of the <b>PerUserInitialization</b> property in the <a href="https://msdn.microsoft.com/41e0d938-00c6-4f4c-8027-8b8512398dee">__Win32Provider</a> instance for the provider.


### -param lFlags [in]

Reserved. This parameter must be 0 (zero).


### -param wszNamespace [in]

A namespace name for which the provider is initialized.


### -param wszLocale [in]

Locale name for which the provider is being initialized.

A string of the following format, where the hex value is a Microsoft standard LCID value:

<ul>
<li>"MS_409"</li>
</ul>
This parameter may be <b>NULL</b>.


### -param pNamespace [in]

An 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> pointer back into Windows Management. This pointer is can service any requests made by the provider. The provider should use the <a href="_com_iunknown_addref">IWbemProviderInit::AddRef</a> method on this pointer if it is going to call back into Windows Management during its execution.


### -param pCtx [in]

An 
<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> pointer associated with initialization. This parameter may be <b>NULL</b>.

If the provider will perform requests back into Windows Management before completing initialization, it should use the <a href="_com_iunknown_addref">IWbemProviderInit::AddRef</a> method on this pointer. For more information, see 
<a href="https://msdn.microsoft.com/5bfd9d9b-ffe5-4def-a97d-85c4c01223f0">Making Calls to WMI</a>.

In the event that a provider must make a dependent request on another provider, you must pass this context string back to WMI to avoid potential lockups. However, in the case of an independent request, this is not necessary, and WMI generates a new context string for it.


### -param pInitSink [in]

An 
<a href="https://msdn.microsoft.com/abcee170-6a28-44d2-97d6-cb62c393b534">IWbemProviderInitSink</a> pointer that is used by the provider to report initialization status.


## -returns



The provider should return <b>WBEM_S_NO_ERROR</b> and indicate its status using the supplied object sink in the <i>pInitSink</i> parameter. However, if a provider returns <b>WBEM_E_FAILED</b> and does not use the sink, then the provider initialization is considered as failed.




## -remarks



Typically, the provider implements a COM object using multiple inheritance to support both the 
<a href="https://msdn.microsoft.com/92edf347-c694-4023-b83f-09531072c631">IWbemProviderInit</a> interface as well as its primary interface, such as 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> or 
<a href="https://msdn.microsoft.com/4b92923a-659d-4340-8843-eb42aea69d47">IWbemEventProvider</a>.

Initialization status is reported by calling 
<a href="https://msdn.microsoft.com/909935ba-ae3a-477d-a466-1f2679764b10">IWbemProviderInitSink::SetStatus</a>. This method can be called repeatedly to report incremental status if necessary. The provider must increment the reference count on this pointer by calling its <a href="_com_iunknown_addref">IWbemProviderInit::AddRef</a> method before using it to communicate status to Windows Management.

The provider may use the 
<a href="https://msdn.microsoft.com/abcee170-6a28-44d2-97d6-cb62c393b534">IWbemProviderInitSink</a> pointer synchronously, as in the following code example.


```cpp
HRESULT SampleProvider::Initialize( 
    /* [unique][in] */  LPWSTR wszUser,
    /* [in] */          LONG lFlags,
    /* [in] */          LPWSTR wszNamespace,
    /* [unique][in] */  LPWSTR wszLocale,
    /* [in] */          IWbemServices __RPC_FAR *pNamespace,
    /* [in] */          IWbemContext __RPC_FAR *pCtx,
    /* [in] */          IWbemProviderInitSink __RPC_FAR *pInitSink
    )
{
    // Use AddRef on the pNamespace pointer, if required.

    // Analyze other parameters.

    // Tell Windows Management that you are initialized.
    pInitSink->SetStatus(WBEM_S_INITIALIZED, 0);
    return WBEM_S_NO_ERROR;
}
```


The provider may also use the <a href="_com_iunknown_addref">AddRef</a> method on the pointer and create a separate thread to complete its initialization and immediately return from the call.

The initialization process of some providers can involve calling back into WMI. A provider that calls back into WMI and must wait for that call to complete is called a dependent provider. Similarly, a call into WMI is called a dependent request. When implementing 
<b>Initialize</b>, WMI requires that a dependent provider obey the following rules:

<ul>
<li>
Dependent requests must reuse the 
<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> pointer that WMI passed to 
<b>Initialize</b>.

This means that any calls into WMI made during initialization must reuse the 
<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> pointer that WMI passed in. Failure to do so can result in deadlock.

</li>
<li>Non-dependent requests must not reuse the 
<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> pointer.</li>
<li>
Dependent providers must make requests to WMI by using one of the following two strategies:

<ol>
<li>Make dependent requests with the thread received from WMI.</li>
<li>Make dependent requests with a new thread created by the provider.</li>
</ol>
</li>
<li>All providers must return the thread received from WMI.</li>
<li>
Under no circumstances does WMI allow a provider to block a thread received from WMI.

The danger in not carefully handling the threads delivered by WMI is that a provider may acquire all the threads in the WMI thread pool and proceed to block those threads. This would result in a deadlocked system.

</li>
</ul>
You may choose to implement your provider in-process. An in-process provider that must connect to WMI separately from the initialization process must use the <b>CLSID_WbemAdministrativeLocator</b> class identifier to access 
<a href="https://msdn.microsoft.com/3e630987-82e3-4eb0-aec0-30562bc7c843">IWbemLocator</a> in a call to <a href="_com_cocreateinstance">CoCreateInstance</a>.

The following code example describes how to use the <b>CLSID_WbemAdministrativeLocator</b> identifier in such a call.


```cpp
  IWbemLocator *pLoc = 0;

  DWORD dwRes = CoCreateInstance(CLSID_WbemAdministrativeLocator, 0, 
      CLSCTX_INPROC_SERVER, IID_IWbemLocator, (LPVOID *) &pLoc);
```


Failure to use the <b>CLSID_WbemAdministrativeLocator</b> identifier results in an Access Denied error. For more information about making a connection to WMI, see 
<a href="https://msdn.microsoft.com/c0d18827-6b36-4817-8cd9-06cd0f267b28">Creating a WMI Application or Script</a>.


#### Examples

The following code example describes how to implement 
<b>Initialize</b> for an event consumer provider.


```cpp
HRESULT CMyEventConsumer::Initialize( 
    /* [in] */ LPWSTR pszUser,
    /* [in] */ LONG lFlags,
    /* [in] */ LPWSTR pszNamespace,
    /* [in] */ LPWSTR pszLocale,
    /* [in] */ IWbemServices __RPC_FAR *pNamespace,
    /* [in] */ IWbemContext __RPC_FAR *pCtx,
    /* [in] */ IWbemProviderInitSink __RPC_FAR *pInitSink
    )
{
    pInitSink->SetStatus(WBEM_S_INITIALIZED, 0);

// Optionally, examine the namespace, locale, and so on 
// being used.

    return WBEM_S_NO_ERROR;
}
```





## -see-also




<a href="https://msdn.microsoft.com/92edf347-c694-4023-b83f-09531072c631">IWbemProviderInit</a>



<a href="https://msdn.microsoft.com/3dc145b8-1ce4-4caa-b2ac-31a3681e76f1">Initializing a Provider</a>
 

 

