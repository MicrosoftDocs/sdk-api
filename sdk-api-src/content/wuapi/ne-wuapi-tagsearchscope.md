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

# tagSearchScope enumeration


## -description


Defines the variety of updates that should be returned by the search: per-machine updates, per-user updates, or both.


## -enum-fields




### -field searchScopeDefault

Search by using the default scope (the scope that Automatic Updates would use when searching for updates). This is currently equivalent to search ScopeMachineOnly.


### -field searchScopeMachineOnly

Search only for per-machine updates; exclude all per-user updates.


### -field searchScopeCurrentUserOnly

Search only for per-user updates applicable to the calling user – the user who owns the process which is making the Windows Update Agent (WUA) API call.


### -field searchScopeMachineAndCurrentUser

[Not currently supported.] Search for per-machine updates and for per-user updates applicable to the current user.


### -field searchScopeMachineAndAllUsers

[Not currently supported.] Search  for per-machine updates and for per-user updates applicable to any known user accounts on the computer.


### -field searchScopeAllUsers

[Not currently supported.] Search only for per-user updates applicable to any known user accounts on the computer. 


## -remarks



In versions of the Windows Update Agent that do not support per-user updates (versions that do not support the <a href="https://msdn.microsoft.com/d37017d5-6f78-4b6c-ac0b-c83b83853079">IUpdateSearcher3</a> interface), searches will always return only per-machine updates.



