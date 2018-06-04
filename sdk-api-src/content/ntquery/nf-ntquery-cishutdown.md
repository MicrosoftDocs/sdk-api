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

# CIShutdown function


## -description


Shuts down the content indexer and closes all open catalogs.
        
            
<div class="alert"><b>Note</b>  This function is not supported as of Windows 8.</div><div> </div>

## -parameters






## -returns



This function does not return a value.




## -remarks



This function does not have an associated header or library file. To use this function, call <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> with the DLL name (Query.dll) to obtain a module handle, and then call <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> with that module handle and an architecture-specific function name to get the address of this function. Specify the function name as "<b>?CIShutdown@@YGXXZ</b>" for x86 architecture, or as "<b>?CIShutdown@@YAXXZ</b>" for x64 architecture.



