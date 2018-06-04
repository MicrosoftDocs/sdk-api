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

# EngFreePrivateUserMem macro


## -description


The <b>EngFreePrivateUserMem</b> function deallocates a block of private user memory.


## -parameters




### -param psl [in]

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a> structure representing the DirectDraw surface with which the memory is associated.


### -param p

TBD






#### - pv [in]

Pointer to the block of user memory being deallocated.


## -remarks



This routine deallocates a block of memory allocated by <a href="https://msdn.microsoft.com/library/windows/hardware/ff564177">EngAllocPrivateUserMem</a>. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564177">EngAllocPrivateUserMem</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564178">EngAllocUserMem</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564912">EngFreeUserMem</a>
 

 

