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

# ITSGAuthenticationEngine::CancelAuthentication


## -description


Cancels an existing authentication request.

Remote Desktop Gateway (RD Gateway) calls this method when the user who initiated the connection terminates the connection, or when the connection fails.


## -parameters




### -param mainSessionId [in]

An identifier assigned to the connection request.


### -param context [in]

A pointer to  a <b>ULONG</b> that contains  a value that identifies this connection. This value should be passed back to RD Gateway by using the methods of the  <a href="https://msdn.microsoft.com/6cc0dca7-1bc7-4229-9f3b-74d600776210">ITSGAuthenticateUserSink</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c72f3f22-a403-45b0-9ccb-6339ae001024">ITSGAuthenticationEngine</a>
 

 

