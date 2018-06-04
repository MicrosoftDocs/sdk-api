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

# CoRevokeInitializeSpy function


## -description


Revokes a registered implementation of the <a href="https://msdn.microsoft.com/9cf1a3fa-dbc6-4760-a9e9-ef237737acfb">IInitializeSpy</a> interface.


## -parameters




### -param uliCookie [in]

A <a href="https://msdn.microsoft.com/83a10c12-2cd1-449a-af3f-b2138fc50ee0">ULARGE_INTEGER</a> cookie identifying the registration.


## -returns



This function can return the standard return value E_INVALIDARG, as well as S_OK to indicate success.





## -remarks



<b>CoRevokeInitializeSpy</b> can only revoke cookies issued by previous calls to <a href="https://msdn.microsoft.com/1fd5606e-0a15-429a-b656-4620b873bec5">CoRegisterInitializeSpy</a> that were executed on the current thread. Using a cookie from another thread, or one that corresponds to an already revoked registration, will return E_INVALIDARG.



It is unpredictable whether a call to <b>CoRevokeInitializeSpy</b> from within an <a href="https://msdn.microsoft.com/9cf1a3fa-dbc6-4760-a9e9-ef237737acfb">IInitializeSpy</a> method call will have an effect during the current top-level (non-nested) call to <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> or <a href="https://msdn.microsoft.com/9411cbed-fa3b-46f7-b677-6ada53324edc">CoUninitialize</a>. The revocation will always have an effect after the current top-level call to <b>CoInitializeEx</b> or <b>CoUninitialize</b> returns.





## -see-also




<a href="https://msdn.microsoft.com/1fd5606e-0a15-429a-b656-4620b873bec5">CoRegisterInitializeSpy</a>



<a href="https://msdn.microsoft.com/9cf1a3fa-dbc6-4760-a9e9-ef237737acfb">IInitializeSpy</a>
 

 

