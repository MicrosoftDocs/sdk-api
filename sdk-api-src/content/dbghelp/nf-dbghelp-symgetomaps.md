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

# SymGetOmaps function


## -description


Retrieves the omap tables within a loaded module.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param BaseOfDll [in]

The base address of the module.


### -param OmapTo [out]

An array of address map entries to the new image layout taken from the original layout. For details on the map entries, see the <a href="https://msdn.microsoft.com/47f1dc1d-9305-4514-83b8-6d32bd9914f2">OMAP</a> structure.


### -param cOmapTo [out]

The number of entries in the <i>OmapTo</i> array.


### -param OmapFrom [out]

An array of address map entries from the new image layout to the original layout (as described by the debug symbols). For details on the map entries, see the <a href="https://msdn.microsoft.com/47f1dc1d-9305-4514-83b8-6d32bd9914f2">OMAP</a> structure.


### -param cOmapFrom [out]

The number of entries in the <i>OmapFrom</i> array.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails (the omap is not found), the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/47f1dc1d-9305-4514-83b8-6d32bd9914f2">OMAP</a>
 

 

