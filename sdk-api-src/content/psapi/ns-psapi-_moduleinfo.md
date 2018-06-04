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

# _MODULEINFO structure


## -description


Contains the module load address, size, and entry point.


## -struct-fields




### -field lpBaseOfDll

The load address of the module.


### -field SizeOfImage

The size of the linear space that the module occupies, in bytes.


### -field EntryPoint

The entry point of the module.


## -remarks



The load address of a module is the same as the <b>HMODULE</b> value. The information returned in the <b>SizeOfImage</b> and <b>EntryPoint</b> members comes from the module's Portable Executable (PE) header. The module entry point is the location called during process startup, thread startup, process shutdown, and thread shutdown. While this is not the address of the 
<a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a> function, it should be close enough for most purposes.




## -see-also




<a href="https://msdn.microsoft.com/afb9f4c8-c8ae-4497-96c1-b559cfa2cedf">GetModuleInformation</a>
 

 

