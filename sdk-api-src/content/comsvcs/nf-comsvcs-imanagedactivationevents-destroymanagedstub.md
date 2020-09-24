---
UID: NF:comsvcs.IManagedActivationEvents.DestroyManagedStub
title: IManagedActivationEvents::DestroyManagedStub (comsvcs.h)
description: Destroys a stub that was created by CreateManagedStub.
helpviewer_keywords: ["DestroyManagedStub","DestroyManagedStub method [COM+]","DestroyManagedStub method [COM+]","IManagedActivationEvents interface","IManagedActivationEvents interface [COM+]","DestroyManagedStub method","IManagedActivationEvents.DestroyManagedStub","IManagedActivationEvents::DestroyManagedStub","_cos_IManagedActivationEvents_DestroyManagedStub","comsvcs/IManagedActivationEvents::DestroyManagedStub","cos.imanagedactivationevents_destroymanagedstub"]
old-location: cos\imanagedactivationevents_destroymanagedstub.htm
tech.root: cos
ms.assetid: aabc8192-d499-441e-be5d-9a51108bd344
ms.date: 12/05/2018
ms.keywords: DestroyManagedStub, DestroyManagedStub method [COM+], DestroyManagedStub method [COM+],IManagedActivationEvents interface, IManagedActivationEvents interface [COM+],DestroyManagedStub method, IManagedActivationEvents.DestroyManagedStub, IManagedActivationEvents::DestroyManagedStub, _cos_IManagedActivationEvents_DestroyManagedStub, comsvcs/IManagedActivationEvents::DestroyManagedStub, cos.imanagedactivationevents_destroymanagedstub
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
 - IManagedActivationEvents::DestroyManagedStub
 - comsvcs/IManagedActivationEvents::DestroyManagedStub
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
 - IManagedActivationEvents.DestroyManagedStub
---

# IManagedActivationEvents::DestroyManagedStub


## -description

Destroys a stub that was created by <a href="/windows/desktop/api/comsvcs/nf-comsvcs-imanagedactivationevents-createmanagedstub">CreateManagedStub</a>.

## -parameters

### -param pInfo [in]

A pointer to <a href="/windows/desktop/api/comsvcs/nn-comsvcs-imanagedobjectinfo">IManagedObjectInfo</a> that describes the stub for a managed object.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imanagedactivationevents">IManagedActivationEvents</a>