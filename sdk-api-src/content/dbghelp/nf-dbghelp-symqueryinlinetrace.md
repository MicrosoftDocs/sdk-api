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

# SymQueryInlineTrace function


## -description


Queries an inline trace.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
      <a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param StartAddress [in]

The start address.


### -param StartContext [in]

Contains the context of the start of block.


### -param StartRetAddress [in]

Contains the return address of the start of the current block/


### -param CurAddress [in]

Contains the current address.


### -param CurContext [out]

Address of a <b>DWORD</b> that receives the current context.


### -param CurFrameIndex [out]

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error 
       information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.


## -remarks



Either the <i>StartAddress</i> or <i>StartRetAddress</i> parameters must be within the same function scope as the <i>CurAddress</i> parameter. The former indicates a step-over within the same function and the latter indicates a step-over from <i>StartAddress</i>.



