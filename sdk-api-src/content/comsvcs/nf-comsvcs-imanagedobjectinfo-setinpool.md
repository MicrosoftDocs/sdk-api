---
UID: NF:comsvcs.IManagedObjectInfo.SetInPool
title: IManagedObjectInfo::SetInPool (comsvcs.h)
description: Sets whether the managed object belongs to the COM+ object pool.
helpviewer_keywords: ["IManagedObjectInfo interface [COM+]","SetInPool method","IManagedObjectInfo.SetInPool","IManagedObjectInfo::SetInPool","SetInPool","SetInPool method [COM+]","SetInPool method [COM+]","IManagedObjectInfo interface","_cos_IManagedObjectInfo_SetInPool","comsvcs/IManagedObjectInfo::SetInPool","cos.imanagedobjectinfo_setinpool"]
old-location: cos\imanagedobjectinfo_setinpool.htm
tech.root: cos
ms.assetid: fef3842f-acf7-4aff-801d-17343633be8c
ms.date: 12/05/2018
ms.keywords: IManagedObjectInfo interface [COM+],SetInPool method, IManagedObjectInfo.SetInPool, IManagedObjectInfo::SetInPool, SetInPool, SetInPool method [COM+], SetInPool method [COM+],IManagedObjectInfo interface, _cos_IManagedObjectInfo_SetInPool, comsvcs/IManagedObjectInfo::SetInPool, cos.imanagedobjectinfo_setinpool
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
 - IManagedObjectInfo::SetInPool
 - comsvcs/IManagedObjectInfo::SetInPool
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
 - IManagedObjectInfo.SetInPool
---

# IManagedObjectInfo::SetInPool


## -description

Sets whether the managed object belongs to the COM+ object pool.

## -parameters

### -param bInPool [in]

Indicates whether the managed object belongs to the COM+ object pool.

### -param pPooledObj [in]

A reference to <a href="/windows/desktop/api/comsvcs/nn-comsvcs-imanagedpooledobj">IManagedPooledObj</a> that describes how this managed object is used in the COM+ object pool.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imanagedobjectinfo">IManagedObjectInfo</a>