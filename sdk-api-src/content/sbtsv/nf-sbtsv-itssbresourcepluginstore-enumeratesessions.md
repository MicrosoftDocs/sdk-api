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

# ITsSbResourcePluginStore::EnumerateSessions


## -description


Enumerates a specified set of sessions.


## -parameters




### -param targetName [in]

The name of the target.


### -param userName [in]

The name of the user account.


### -param userDomain [in]

The domain name of the user account.


### -param poolName [in]

The name of the pool.


### -param initialProgram [in]

The name of the published remote application.


### -param pSessionState [in]

A pointer to the  <a href="https://msdn.microsoft.com/2780e704-72f1-44a9-ad54-ab3d2b19befe">TSSESSION_STATE</a> value of the sessions to enumerate.


### -param pdwCount [in, out]

Returns a pointer to the number of sessions returned.


### -param ppVal [out]

Returns the list of sessions requested.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a>



<a href="https://msdn.microsoft.com/768a5a4e-8221-417a-ad65-9a213a176eca">ITsSbResourcePluginStoreEx</a>
 

 

