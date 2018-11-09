---
UID: NF:objidl.IBlockingLock.Lock
title: IBlockingLock::Lock
author: windows-sdk-content
description: Requests a lock on a shared resource.
old-location: com\iblockinglock_lock.htm
tech.root: com
ms.assetid: 35657795-2f18-4738-b0b5-8d03e0e4179d
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IBlockingLock interface [COM],Lock method, IBlockingLock.Lock, IBlockingLock::Lock, Lock, Lock method [COM], Lock method [COM],IBlockingLock interface, _com_iblockinglock_lock, com.iblockinglock_lock, objidl/IBlockingLock::Lock
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - ObjIdl.h
api_name:
 - IBlockingLock.Lock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBlockingLock::Lock


## -description


Requests a lock on a shared resource.


## -parameters




### -param dwTimeout [in]

The time interval after which the attempted lock operation fails.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/8fccc4f9-17fe-4927-b00d-2815f47857e5">IBlockingLock</a>
 

 

