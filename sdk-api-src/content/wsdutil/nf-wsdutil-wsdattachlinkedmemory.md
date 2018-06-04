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

# WSDAttachLinkedMemory function


## -description


Attaches a child memory block to a
parent memory block. Multiple children can be attached to a parent memory block.


## -parameters




### -param pParent

Pointer to the parent memory block.


### -param pChild

Pointer to the child memory block.


## -returns



This function does not return a value.




## -remarks



The child memory block is automatically freed when the parent memory
block is freed. Both the parent and child memory blocks must have been previously allocated by calls to <a href="https://msdn.microsoft.com/2608985f-56aa-4223-b76d-85ebe3b080fb">WSDAllocateLinkedMemory</a>.



