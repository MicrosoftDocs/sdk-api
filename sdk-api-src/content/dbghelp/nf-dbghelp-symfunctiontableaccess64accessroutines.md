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

# SymFunctionTableAccess64AccessRoutines function


## -description


 Finds a function table entry or  frame pointer omission (FPO) record for an address.

Use <a href="https://msdn.microsoft.com/f79e6af9-9931-4bd7-ae12-29d890267a89">SymFunctionTableAccess64</a> instead.


## -parameters




### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param AddrBase [in]

The base address for which function table information is required.


### -param ReadMemoryRoutine [in, optional]

Pointer to a read memory callback function.


### -param GetModuleBaseRoutine [in, optional]

Pointer to a get module base callback function.


## -see-also




<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a>
 

 

