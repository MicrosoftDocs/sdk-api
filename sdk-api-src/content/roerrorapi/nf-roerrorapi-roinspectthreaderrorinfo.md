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

# RoInspectThreadErrorInfo function


## -description


Gets the error object that represents the call stack at the point where the error originated


## -parameters




### -param targetTebAddress [in]

The target thread environment block (TEB).


### -param machine

The machine to debug.


### -param readMemoryCallback

A callback function to read the buffer from the target TEB address space.


### -param context [in, optional]

Custom context data.


### -param targetErrorInfoAddress [out]

The address of the error object.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When the call to <b>RoInspectThreadErrorInfo</b> is  successful, <i>targetErrorInfoAddress</i> contains the address of an error object that you can pass to the <a href="https://msdn.microsoft.com/2C5B04DD-888B-4400-A01D-CDF9DD870584">RoInspectCapturedStackBackTrace</a> function to get the call stack at the point where the error was originated.




## -see-also




<a href="https://msdn.microsoft.com/A5BF207D-BB8D-47C1-8D32-0B6494809E2B">PINSPECT_MEMORY_CALLBACK</a>



<a href="https://msdn.microsoft.com/2C5B04DD-888B-4400-A01D-CDF9DD870584">RoInspectCapturedStackBackTrace</a>
 

 

