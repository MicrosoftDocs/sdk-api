---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWbemProviderInitSink::SetStatus


## -description


The 
<b>IWbemProviderInitSink::SetStatus</b> method indicates to Windows Management whether a provider is fully or partially initialized.


## -parameters




### -param lStatus [in]

Indicates to Windows Management a provider's initialization status. One of the following values can be set.



#### WBEM_S_INITIALIZED

Indicates that the provider is fully initialized and ready to accept requests.



#### WBEM_E_FAILED

Indicates that the provider has failed to initialize and is not functional.


### -param lFlags [in]

Reserved. This parameter must be 0 (zero).


## -returns



This method always returns <b>WBEM_S_NO_ERROR</b>.




## -remarks



All types of providers call 
<b>IWbemProviderInitSink::SetStatus</b> to indicate initialization status to Windows Management.

If <i>lStatus</i> is set to <b>WBEM_S_INITIALIZED</b>, Windows Management expects the provider to be fully capable of immediately servicing requests.




## -see-also




<a href="https://msdn.microsoft.com/abcee170-6a28-44d2-97d6-cb62c393b534">IWbemProviderInitSink</a>



<a href="https://msdn.microsoft.com/3dc145b8-1ce4-4caa-b2ac-31a3681e76f1">Initializing a Provider</a>
 

 

