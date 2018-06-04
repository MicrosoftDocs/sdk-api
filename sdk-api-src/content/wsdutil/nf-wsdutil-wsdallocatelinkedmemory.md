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

# WSDAllocateLinkedMemory function


## -description


Allocates a linked memory block.


## -parameters




### -param pParent

 Pointer to the parent memory block.


### -param cbSize

Size of the memory block to be allocated.


## -returns



Pointer to the newly allocated memory block.




## -remarks



The memory 
block allocated by <b>WSDAllocateLinkedMemory</b> is linked to a parent memory block and is freed when 
the parent memory block is freed.

 If <i>pParent</i> is <b>NULL</b> the allocated memory block must be explicitly freed by calling 
<a href="https://msdn.microsoft.com/8fe6f586-a262-4248-9650-dec0fae8cd74">WSDFreeLinkedMemory</a>.



