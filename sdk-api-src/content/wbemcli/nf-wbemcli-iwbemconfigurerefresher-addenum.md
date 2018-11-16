---
UID: NF:wbemcli.IWbemConfigureRefresher.AddEnum
title: IWbemConfigureRefresher::AddEnum
author: windows-sdk-content
description: The IWbemConfigureRefresher::AddEnum method adds an enumerator to the requested refresher.
old-location: wmi\iwbemconfigurerefresher_addenum.htm
tech.root: WmiSdk
ms.assetid: 5b013267-78bc-4372-b55a-58e330acf927
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AddEnum, AddEnum method [Windows Management Instrumentation], AddEnum method [Windows Management Instrumentation],IWbemConfigureRefresher interface, IWbemConfigureRefresher interface [Windows Management Instrumentation],AddEnum method, IWbemConfigureRefresher.AddEnum, IWbemConfigureRefresher::AddEnum, _hmm_iwbemconfigurerefresher_addenum, wbemcli/IWbemConfigureRefresher::AddEnum, wmi.iwbemconfigurerefresher_addenum
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
 - IWbemConfigureRefresher.AddEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wbemcli.h
: 
- IWbemConfigureRefresher.AddEnum
: 
---

# IWbemConfigureRefresher::AddEnum


## -description


The 
<b>IWbemConfigureRefresher::AddEnum</b> method adds an enumerator to the requested refresher.


## -parameters




### -param pNamespace [in]

An 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> pointer back into Windows Management, which can service any request made by the provider. If the method must call back into Windows Management during its execution, the provider should call <a href="https://msdn.microsoft.com/en-us/library/ms691379(v=VS.85).aspx">AddRef</a> with the <i>pNamespace</i> pointer.


### -param wszClassName [in]

Constant, null-terminated string of 16-bit Unicode characters containing the name of the class that is enumerated.


### -param lFlags [in]

Bitmask of flags that modify the behavior of this method. If this parameter is set to WBEM_FLAG_USE_AMENDED_QUALIFIERS, the returned instances contain localized qualifiers if they are available.


### -param pContext [in]

Typically <b>NULL</b>; otherwise, this is a pointer to an 
<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> object that is required by one or more dynamic class providers. The values in the context object must be specified in the specific provider documentation. For more information about this parameter, see 
<a href="https://msdn.microsoft.com/5bfd9d9b-ffe5-4def-a97d-85c4c01223f0">Making Calls to WMI</a>.


### -param ppEnum [out]

Pointer that holds the reference to a 
<a href="https://msdn.microsoft.com/71ce1c89-446e-4137-9857-9d3c5921e0b7">IWbemHiPerfEnum</a> object, which will contain the enumeration. The client must call <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">Release</a> on this pointer when it is no longer required.


### -param plId [out]

Pointer to an integer returned by the provider that uniquely identifies the refreshable enumeration.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <div class="alert"><b>Note</b>  <b>HRESULT</b></div>
<div> </div>.




## -remarks



The supplied class must specify a valid class, which is provided by the High-Performance Provider. All instances of the returned enumerator can be queried after calls. On each call to refresh, the number of instances in the enumerator can vary. Only instances of the specified class name are returned; subclasses of the specified class will not be enumerated because detailed enumeration is not supported. The returned enumerator must not be touched by the client while a 
<a href="https://msdn.microsoft.com/6de85040-c938-41dc-8240-0e21e89c7716">Refresh</a> operation is in process. The returned identifier can be used by the 
<a href="https://msdn.microsoft.com/f6e68b95-e9d1-473e-add4-823b6db51709">Remove</a> function to remove the object. Note that it is not necessary for the user to explicitly remove added enumerators. However, the client must call <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">Release</a> on the returned enumerator when it is no longer required.




## -see-also




<a href="https://msdn.microsoft.com/9dd56891-5f2f-4b0e-9f70-fd75cb9bbd43">IWbemConfigureRefresher</a>
 

 

