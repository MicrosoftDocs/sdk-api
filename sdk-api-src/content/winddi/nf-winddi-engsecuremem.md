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

# EngSecureMem function


## -description


The <b>EngSecureMem</b> function locks down the specified address range in memory.


## -parameters




### -param Address [in]

Pointer to the base address of the memory to be secured.


### -param Length [in]

Specifies the size of the memory range to be secured.


## -returns



<b>EngSecureMem</b> returns a handle to the secured address range upon successful completion; otherwise, it returns <b>NULL</b>.




## -remarks



The address range locked down by <b>EngSecureMem</b> will not be deallocated until it is unlocked by <a href="https://msdn.microsoft.com/library/windows/hardware/ff565454">EngUnsecureMem</a>.



