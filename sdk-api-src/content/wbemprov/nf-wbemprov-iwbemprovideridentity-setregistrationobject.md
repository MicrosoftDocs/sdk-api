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

# IWbemProviderIdentity::SetRegistrationObject


## -description


The 
<b>IWbemProviderIdentity::SetRegistrationObject</b> method is called by the Windows Management service prior to initializing an event provider (if the provider implements 
<a href="https://msdn.microsoft.com/872daa72-c6ff-4c6d-a870-c32e3688eb13">IWbemProviderIdentity</a>). The method is used to pass to the provider the 
<a href="https://msdn.microsoft.com/41e0d938-00c6-4f4c-8027-8b8512398dee">__Win32Provider</a> instance by which the provider is being initialized. This method is only used if you have more than one provider sharing the same <b>CLSID</b>.


## -parameters




### -param lFlags [in]

Reserved. This parameter must be 0 (zero).


### -param pProvReg [in]

Instance of 
<a href="https://msdn.microsoft.com/41e0d938-00c6-4f4c-8027-8b8512398dee">__Win32Provider</a> that announces the provider's name and <b>CLSID</b>.


## -returns



This method returns an <b>HRESULT</b> with one of the following values.




## -remarks



Any <b>HRESULT</b> return code other than <b>WBEM_S_NO_ERROR</b> indicates a provider failure.




## -see-also




<a href="https://msdn.microsoft.com/872daa72-c6ff-4c6d-a870-c32e3688eb13">IWbemProviderIdentity</a>
 

 

