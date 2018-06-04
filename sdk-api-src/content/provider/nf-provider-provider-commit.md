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

# Provider::Commit


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>Commit</b> method is used to send an instance to WMI. This method is a helper function and should not be overridden.


## -parameters




### -param pInstance

Pointer to the instance to be stored by WMI.


### -param bCache

Indicates whether a cache is implemented. This value must be set to <b>FALSE</b> in the current version of the provider framework.


## -returns



Use the <b>SUCCEEDED</b> or <b>FAILED</b> macros on the returned HRESULT to determine if the method was successful.




## -remarks



If the client cancels the query, the <b>Commit</b> method returns an error. A provider writer can use this fact to terminate an enumeration.

Also, this method calls CInstance::Release on the <i>pInstance</i> pointer. Because of this, the framework provider must be careful not to call CInstance::Release again. This means that a <i>pInstance</i> smart pointer is incompatible with this method because the smart pointer calls CInstance::Release in its destructor.

This method should only be used when the framework provider does not call CInstance::Release on the <i>pInstance</i> pointer separately and if the <i>pInstance</i> pointer is not, and will never be, a smart pointer.



