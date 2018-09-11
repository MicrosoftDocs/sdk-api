---
UID: NF:comsvcs.IManagedActivationEvents.DestroyManagedStub
title: IManagedActivationEvents::DestroyManagedStub
author: windows-sdk-content
description: Destroys a stub that was created by CreateManagedStub.
old-location: cos\imanagedactivationevents_destroymanagedstub.htm
tech.root: cossdk
ms.assetid: aabc8192-d499-441e-be5d-9a51108bd344
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DestroyManagedStub, DestroyManagedStub method [COM+], DestroyManagedStub method [COM+],IManagedActivationEvents interface, IManagedActivationEvents interface [COM+],DestroyManagedStub method, IManagedActivationEvents.DestroyManagedStub, IManagedActivationEvents::DestroyManagedStub, _cos_IManagedActivationEvents_DestroyManagedStub, comsvcs/IManagedActivationEvents::DestroyManagedStub, cos.imanagedactivationevents_destroymanagedstub
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IManagedActivationEvents.DestroyManagedStub
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IManagedActivationEvents::DestroyManagedStub


## -description


Destroys a stub that was created by <a href="https://msdn.microsoft.com/a2ba7ece-ac17-42fb-b22f-976ad849eca5">CreateManagedStub</a>.


## -parameters




### -param pInfo [in]

A pointer to <a href="https://msdn.microsoft.com/7fa5f76e-df07-41b3-8fb0-62b84a034aa5">IManagedObjectInfo</a> that describes the stub for a managed object.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms681786(v=VS.85).aspx">IManagedActivationEvents</a>
 

 

