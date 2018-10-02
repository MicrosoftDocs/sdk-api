---
UID: NF:wbemcli.IWbemConfigureRefresher.AddObjectByPath
title: IWbemConfigureRefresher::AddObjectByPath
author: windows-sdk-content
description: The IWbemConfigureRefresher::AddObjectByPath method adds an object to a refresher by specifying an object path.
old-location: wmi\iwbemconfigurerefresher_addobjectbypath.htm
tech.root: WmiSdk
ms.assetid: 85721e0c-863b-45af-91ca-8ee14af37181
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: AddObjectByPath, AddObjectByPath method [Windows Management Instrumentation], AddObjectByPath method [Windows Management Instrumentation],IWbemConfigureRefresher interface, IWbemConfigureRefresher interface [Windows Management Instrumentation],AddObjectByPath method, IWbemConfigureRefresher.AddObjectByPath, IWbemConfigureRefresher::AddObjectByPath, _hmm_iwbemconfigurerefresher_addobjectbypath, wbemcli/IWbemConfigureRefresher::AddObjectByPath, wmi.iwbemconfigurerefresher_addobjectbypath
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemuuid.lib
 - Wbemuuid.dll
api_name:
 - IWbemConfigureRefresher.AddObjectByPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemConfigureRefresher::AddObjectByPath


## -description


The 
<b>IWbemConfigureRefresher::AddObjectByPath</b> method adds an object to a refresher by specifying an object path.


## -parameters




### -param pNamespace [in]

An 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> pointer back into Windows Management, which can service any request made by the provider. The provider should call <a href="_com_iunknown_addref">AddRef</a> on this pointer if it is going to call back into Windows Management during its execution.


### -param wszPath [in]

Constant, null-terminated string of 16-bit Unicode characters that contains the object path of the object you add to the refresher.


### -param lFlags [in]

Bitmask of flags that modify the behavior of this method. If this parameter is set to <b>WBEM_FLAG_USE_AMENDED_QUALIFIERS</b>, the returned instance contain localized qualifiers if available.


### -param pContext

TBD


### -param ppRefreshable [out]

Pointer to hold the reference to a 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> object, which contains the refreshable instance object. The client must call <a href="_com_iunknown_release">Release</a> on the returned object when it is no longer required.


### -param plId [out]

Pointer to an integer returned by the provider that uniquely identifies the refreshable object.


#### - pCtx [in]

Typically <b>NULL</b>; otherwise, a pointer to an 
<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> object that is required by one or more dynamic class providers. The values in the context object must be specified in the specific provider documentation. For more information about this parameter, see 
<a href="https://msdn.microsoft.com/5bfd9d9b-ffe5-4def-a97d-85c4c01223f0">Making Calls to WMI</a>.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




## -remarks



The supplied path must specify a valid object, which is provided by the High-Performance Provider. The returned object must not be touched by the client while a refresh operation is in process. The returned identifier can be used by the 
<a href="https://msdn.microsoft.com/f6e68b95-e9d1-473e-add4-823b6db51709">Remove</a> function to remove the object.

<div class="alert"><b>Note</b>  It is not necessary for the user to explicitly remove added objects. The client must call <a href="_com_iunknown_release">Release</a> on the returned object when it is no longer required.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/ee0a2ead-f53a-4651-a287-04a62eba3f84">Accessing Performance Data in C++</a>



<a href="https://msdn.microsoft.com/9dd56891-5f2f-4b0e-9f70-fd75cb9bbd43">IWbemConfigureRefresher</a>



<a href="https://msdn.microsoft.com/6a22d6f7-d9e2-45fa-876d-921a4bc4f574">Making an Instance Provider into a High-Performance Provider</a>



<a href="https://msdn.microsoft.com/2c7206e7-f5f8-4d40-b993-56122e48069b">Performance Counter Provider</a>
 

 

