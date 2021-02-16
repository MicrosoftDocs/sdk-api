---
UID: NF:comsvcs.IManagedActivationEvents.CreateManagedStub
title: IManagedActivationEvents::CreateManagedStub (comsvcs.h)
description: Creates a stub for a managed object within the current COM+ context.
helpviewer_keywords: ["CreateManagedStub","CreateManagedStub method [COM+]","CreateManagedStub method [COM+]","IManagedActivationEvents interface","IManagedActivationEvents interface [COM+]","CreateManagedStub method","IManagedActivationEvents.CreateManagedStub","IManagedActivationEvents::CreateManagedStub","_cos_IManagedActivationEvents_CreateManagedStub","comsvcs/IManagedActivationEvents::CreateManagedStub","cos.imanagedactivationevents_createmanagedstub"]
old-location: cos\imanagedactivationevents_createmanagedstub.htm
tech.root: cos
ms.assetid: a2ba7ece-ac17-42fb-b22f-976ad849eca5
ms.date: 12/05/2018
ms.keywords: CreateManagedStub, CreateManagedStub method [COM+], CreateManagedStub method [COM+],IManagedActivationEvents interface, IManagedActivationEvents interface [COM+],CreateManagedStub method, IManagedActivationEvents.CreateManagedStub, IManagedActivationEvents::CreateManagedStub, _cos_IManagedActivationEvents_CreateManagedStub, comsvcs/IManagedActivationEvents::CreateManagedStub, cos.imanagedactivationevents_createmanagedstub
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IManagedActivationEvents::CreateManagedStub
 - comsvcs/IManagedActivationEvents::CreateManagedStub
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IManagedActivationEvents.CreateManagedStub
---

# IManagedActivationEvents::CreateManagedStub


## -description

Creates a stub for a managed object within the current COM+ context.

## -parameters

### -param pInfo [in]

A pointer to <a href="/windows/desktop/api/comsvcs/nn-comsvcs-imanagedobjectinfo">IManagedObjectInfo</a> that describes the stub for a managed object.

### -param fDist [in]

Indicates whether the created stub is the distinguished stub. A distinguished stub is the stub that controls the lifetime of the current COM+ context.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imanagedactivationevents">IManagedActivationEvents</a>