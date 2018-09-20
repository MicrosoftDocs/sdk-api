---
UID: NF:wbemcli.IWbemConfigureRefresher.AddObjectByTemplate
title: IWbemConfigureRefresher::AddObjectByTemplate
author: windows-sdk-content
description: With the IWbemConfigureRefresher::AddObjectByTemplate method, you can add an object you want refreshed to a refresher by specifying an IWbemClassObject instance template.
old-location: wmi\iwbemconfigurerefresher_addobjectbytemplate.htm
tech.root: WmiSdk
ms.assetid: c3f25484-7c6c-4625-9d26-1c01d15b10c4
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: AddObjectByTemplate, AddObjectByTemplate method [Windows Management Instrumentation], AddObjectByTemplate method [Windows Management Instrumentation],IWbemConfigureRefresher interface, IWbemConfigureRefresher interface [Windows Management Instrumentation],AddObjectByTemplate method, IWbemConfigureRefresher.AddObjectByTemplate, IWbemConfigureRefresher::AddObjectByTemplate, _hmm_iwbemconfigurerefresher_addobjectbytemplate, wbemcli/IWbemConfigureRefresher::AddObjectByTemplate, wmi.iwbemconfigurerefresher_addobjectbytemplate
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
 - IWbemConfigureRefresher.AddObjectByTemplate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemConfigureRefresher::AddObjectByTemplate


## -description


With the 
<b>IWbemConfigureRefresher::AddObjectByTemplate</b> method, you can add an object you want refreshed to a refresher by specifying an 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> instance template. Use this method when it is difficult to construct an object path for an object to add to a refresher.
<div class="alert"><b>Note</b>  The key properties of the instance object must be filled out before you can call the 
<b>AddObjectByTemplate</b> method.</div><div> </div>

## -parameters




### -param pNamespace

An 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> pointer back into Windows Management, which can service any request made by the provider. The provider should call <a href="_com_iunknown_addref">AddRef</a> on this pointer if it is going to call back into Windows Management during its execution.


### -param pTemplate [in]

Pointer to a 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> object that contains the instance template.


### -param lFlags [in]

Bitmask of flags that modify the behavior of this method. If this parameter is set to <b>WBEM_FLAG_USE_AMENDED_QUALIFIERS</b>, the returned instance will contain localized qualifiers if available.


### -param pContext

TBD


### -param ppRefreshable [out]

Pointer to hold the reference to a 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> object, which will contain the refreshable instance object. The client must call <a href="_com_iunknown_release">Release</a> on the returned object when it is no longer required.


### -param plId

TBD




#### - pCtx [in]

Typically <b>NULL</b>; otherwise, a pointer to an 
<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> object that is required by one or more dynamic class providers. The values in the context object must be specified in the specific provider documentation. For more information about this parameter, see 
<a href="https://msdn.microsoft.com/5bfd9d9b-ffe5-4def-a97d-85c4c01223f0">Making Calls to WMI</a>.


#### - plid [out]

Pointer to an integer returned by the provider that uniquely identifies this refreshable object.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




## -remarks



The supplied instance must specify a valid object, which is provided by the High-Performance Provider. The returned object must not be modified by the client while a refresh operation is in process. The returned identifier can be used by the 
<a href="https://msdn.microsoft.com/f6e68b95-e9d1-473e-add4-823b6db51709">Remove</a> function to remove the object.

It is not necessary for the user to explicitly remove added objects. The client must call <a href="_com_iunknown_release">Release</a> on the returned object when it is no longer required.




## -see-also




<a href="https://msdn.microsoft.com/ee0a2ead-f53a-4651-a287-04a62eba3f84">Accessing Performance Data in C++</a>



<a href="https://msdn.microsoft.com/9dd56891-5f2f-4b0e-9f70-fd75cb9bbd43">IWbemConfigureRefresher</a>



<a href="https://msdn.microsoft.com/6a22d6f7-d9e2-45fa-876d-921a4bc4f574">Making an Instance Provider into a High-Performance Provider</a>



<a href="https://msdn.microsoft.com/2c7206e7-f5f8-4d40-b993-56122e48069b">Performance Counter Provider</a>
 

 

