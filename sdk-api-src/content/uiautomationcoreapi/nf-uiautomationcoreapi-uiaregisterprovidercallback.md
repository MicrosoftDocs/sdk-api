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

# UiaRegisterProviderCallback function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Registers the application-defined method that is called by UI Automation 
		to obtain a provider for an element.


## -parameters




### -param pCallback

TBD




#### - pCallBack [in]

Type: <b><a href="https://msdn.microsoft.com/45a32e14-9b8b-452e-a2eb-0f6773980f2f">UiaProviderCallback</a>*</b>

The address of the <a href="https://msdn.microsoft.com/45a32e14-9b8b-452e-a2eb-0f6773980f2f">UiaProviderCallback</a> callback function that returns the provider.


## -returns



This function does not return a value.



