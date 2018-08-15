---
UID: NF:comsvcs.IManagedPooledObj.SetHeld
title: IManagedPooledObj::SetHeld
author: windows-sdk-content
description: Sets whether the managed object should go back into the COM+ object pool.
old-location: cos\imanagedpooledobj_setheld.htm
old-project: cossdk
ms.assetid: 36e7f210-0532-424f-b958-a7a1be904b3c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IManagedPooledObj interface [COM+],SetHeld method, IManagedPooledObj.SetHeld, IManagedPooledObj::SetHeld, SetHeld, SetHeld method [COM+], SetHeld method [COM+],IManagedPooledObj interface, _cos_IManagedPooledObj_SetHeld, comsvcs/IManagedPooledObj::SetHeld, cos.imanagedpooledobj_setheld
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IManagedPooledObj.SetHeld
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IManagedPooledObj::SetHeld


## -description


Sets whether the managed object should go back into the COM+ object pool.


## -parameters




### -param m_bHeld






#### - bHeld [in]

Indicates whether the managed object should go back into the COM+ object pool.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/04853859-5d85-4b88-9e1b-422e3454fd3f">IManagedPooledObj</a>
 

 

