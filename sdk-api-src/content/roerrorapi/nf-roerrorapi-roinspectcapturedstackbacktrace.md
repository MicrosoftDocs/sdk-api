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

# RoInspectCapturedStackBackTrace function


## -description


Provides a way to for debuggers to inspect a call stack from a target process.


## -parameters




### -param targetErrorInfoAddress [in]

The address of the error info object in the target process. Get the <i>targetErrorInfoAddress</i> by calling the <a href="https://msdn.microsoft.com/DE7A930A-89CD-45C0-A232-800E5A5648F8">RoInspectThreadErrorInfo</a> function.


### -param machine

The machine to debug.


### -param readMemoryCallback

A callback function to read the buffer from the target TEB address space.


### -param context [in, optional]

Custom context data.


### -param frameCount [out]

The number of stack frames stored in the error object.


### -param targetBackTraceAddress [out]

The stack back trace address in the target process.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>RoInspectCapturedStackBackTrace</b> function takes a pointer to a system error object  and fills <i>frameCount</i> with the number of stack frames stored in the error object,  and it fills <i>targetBackTraceAddress</i> with the stack back trace address in the target process. The <b>RoInspectCapturedStackBackTrace</b> function tries to confirm that <i>targetErrorInfoAddress</i> points is to a system error object and fails if it can't match the version signature.

Get the <i>targetErrorInfoAddress</i> by calling the <a href="https://msdn.microsoft.com/DE7A930A-89CD-45C0-A232-800E5A5648F8">RoInspectThreadErrorInfo</a> function.




## -see-also




<a href="https://msdn.microsoft.com/A5BF207D-BB8D-47C1-8D32-0B6494809E2B">PINSPECT_MEMORY_CALLBACK</a>



<a href="https://msdn.microsoft.com/DE7A930A-89CD-45C0-A232-800E5A5648F8">RoInspectThreadErrorInfo</a>
 

 

