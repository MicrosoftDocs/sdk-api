---
UID: NF:comsvcs.IManagedPooledObj.SetHeld
title: IManagedPooledObj::SetHeld (comsvcs.h)
description: Sets whether the managed object should go back into the COM+ object pool.
helpviewer_keywords: ["IManagedPooledObj interface [COM+]","SetHeld method","IManagedPooledObj.SetHeld","IManagedPooledObj::SetHeld","SetHeld","SetHeld method [COM+]","SetHeld method [COM+]","IManagedPooledObj interface","_cos_IManagedPooledObj_SetHeld","comsvcs/IManagedPooledObj::SetHeld","cos.imanagedpooledobj_setheld"]
old-location: cos\imanagedpooledobj_setheld.htm
tech.root: cos
ms.assetid: 36e7f210-0532-424f-b958-a7a1be904b3c
ms.date: 12/05/2018
ms.keywords: IManagedPooledObj interface [COM+],SetHeld method, IManagedPooledObj.SetHeld, IManagedPooledObj::SetHeld, SetHeld, SetHeld method [COM+], SetHeld method [COM+],IManagedPooledObj interface, _cos_IManagedPooledObj_SetHeld, comsvcs/IManagedPooledObj::SetHeld, cos.imanagedpooledobj_setheld
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
 - IManagedPooledObj::SetHeld
 - comsvcs/IManagedPooledObj::SetHeld
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
 - IManagedPooledObj.SetHeld
---

# IManagedPooledObj::SetHeld


## -description

Sets whether the managed object should go back into the COM+ object pool.

## -parameters

### -param m_bHeld [in]

Indicates whether the managed object should go back into the COM+ object pool.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imanagedpooledobj">IManagedPooledObj</a>