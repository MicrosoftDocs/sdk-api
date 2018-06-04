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

# ImagehlpApiVersion function


## -description


Retrieves the version information of the DbgHelp library installed on the system.

To indicate the version of the library with which the application was built, use the 
<a href="https://msdn.microsoft.com/86a26160-ebad-4d6e-b559-3d59f2beb5ca">ImagehlpApiVersionEx</a> function.


## -parameters






## -returns




						The return value is a pointer to an 
<a href="https://msdn.microsoft.com/f983f639-6a94-4b83-a443-0d98b85d3950">API_VERSION</a> structure.
					




## -remarks



Use the information in the 
<a href="https://msdn.microsoft.com/f983f639-6a94-4b83-a443-0d98b85d3950">API_VERSION</a> structure to determine whether the version of the library installed on the system is compatible with the version of the library used by the application. Although the library functions are backward compatible, functions introduced in one version are obviously not available in earlier versions.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/f983f639-6a94-4b83-a443-0d98b85d3950">API_VERSION</a>



<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/86a26160-ebad-4d6e-b559-3d59f2beb5ca">ImagehlpApiVersionEx</a>
 

 

