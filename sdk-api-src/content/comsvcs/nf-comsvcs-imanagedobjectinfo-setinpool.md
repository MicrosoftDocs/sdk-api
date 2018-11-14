---
UID: NF:comsvcs.IManagedObjectInfo.SetInPool
title: IManagedObjectInfo::SetInPool
author: windows-sdk-content
description: Sets whether the managed object belongs to the COM+ object pool.
old-location: cos\imanagedobjectinfo_setinpool.htm
tech.root: cossdk
ms.assetid: fef3842f-acf7-4aff-801d-17343633be8c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IManagedObjectInfo interface [COM+],SetInPool method, IManagedObjectInfo.SetInPool, IManagedObjectInfo::SetInPool, SetInPool, SetInPool method [COM+], SetInPool method [COM+],IManagedObjectInfo interface, _cos_IManagedObjectInfo_SetInPool, comsvcs/IManagedObjectInfo::SetInPool, cos.imanagedobjectinfo_setinpool
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
 - IManagedObjectInfo.SetInPool
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- comsvcs.h
: 
- IManagedObjectInfo.SetInPool
: 
---

# IManagedObjectInfo::SetInPool


## -description


Sets whether the managed object belongs to the COM+ object pool.


## -parameters




### -param bInPool [in]

Indicates whether the managed object belongs to the COM+ object pool.


### -param pPooledObj [in]

A reference to <a href="https://msdn.microsoft.com/04853859-5d85-4b88-9e1b-422e3454fd3f">IManagedPooledObj</a> that describes how this managed object is used in the COM+ object pool.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/7fa5f76e-df07-41b3-8fb0-62b84a034aa5">IManagedObjectInfo</a>
 

 

