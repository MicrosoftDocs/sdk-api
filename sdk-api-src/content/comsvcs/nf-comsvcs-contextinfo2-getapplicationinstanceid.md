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

# ContextInfo2::GetApplicationInstanceId


## -description


Retrieves the GUID of the application instance of the current object context.

This information is useful when using <a href="https://msdn.microsoft.com/b0ae1b52-b0c5-4f1c-94c6-628d39ef40e3">COM+ Application Recycling</a>, for example.



## -parameters




### -param __MIDL__ContextInfo20002






#### - pbstrAppInstID [out]

A reference to the application instance identifier.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/06954cc5-19a7-4bae-ac30-94dcdc35d15d">ContextInfo2</a>
 

 

