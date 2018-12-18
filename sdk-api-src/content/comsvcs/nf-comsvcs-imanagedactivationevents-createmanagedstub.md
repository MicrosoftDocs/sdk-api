---
UID: NF:comsvcs.IManagedActivationEvents.CreateManagedStub
title: IManagedActivationEvents::CreateManagedStub
author: windows-sdk-content
description: Creates a stub for a managed object within the current COM+ context.
old-location: cos\imanagedactivationevents_createmanagedstub.htm
tech.root: cossdk
ms.assetid: a2ba7ece-ac17-42fb-b22f-976ad849eca5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateManagedStub, CreateManagedStub method [COM+], CreateManagedStub method [COM+],IManagedActivationEvents interface, IManagedActivationEvents interface [COM+],CreateManagedStub method, IManagedActivationEvents.CreateManagedStub, IManagedActivationEvents::CreateManagedStub, _cos_IManagedActivationEvents_CreateManagedStub, comsvcs/IManagedActivationEvents::CreateManagedStub, cos.imanagedactivationevents_createmanagedstub
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IManagedActivationEvents.CreateManagedStub
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IManagedActivationEvents::CreateManagedStub


## -description


Creates a stub for a managed object within the current COM+ context.


## -parameters




### -param pInfo [in]

A pointer to <a href="https://msdn.microsoft.com/7fa5f76e-df07-41b3-8fb0-62b84a034aa5">IManagedObjectInfo</a> that describes the stub for a managed object.


### -param fDist [in]

Indicates whether the created stub is the distinguished stub. A distinguished stub is the stub that controls the lifetime of the current COM+ context.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/621ffc7d-186e-451c-8d97-9c8291549f51">IManagedActivationEvents</a>
 

 

