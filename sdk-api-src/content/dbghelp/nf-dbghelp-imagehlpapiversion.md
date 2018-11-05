---
UID: NF:dbghelp.ImagehlpApiVersion
title: ImagehlpApiVersion function
author: windows-sdk-content
description: Retrieves the version information of the DbgHelp library installed on the system.
old-location: base\imagehlpapiversion.htm
tech.root: debug
ms.assetid: 0ad9a047-f2ae-4fbe-8a85-9817a616ef73
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ImagehlpApiVersion, ImagehlpApiVersion function, _win32_imagehlpapiversion, base.imagehlpapiversion, dbghelp/ImagehlpApiVersion
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
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
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
api_name:
 - ImagehlpApiVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
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
 

 

