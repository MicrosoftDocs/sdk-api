---
UID: NF:dbghelp.EnumerateLoadedModulesExW
title: EnumerateLoadedModulesExW function
author: windows-sdk-content
description: Enumerates the loaded modules for the specified process.
old-location: base\enumerateloadedmodulesex.htm
tech.root: debug
ms.assetid: 4d3d7460-7a84-4d8b-8cea-c6773beac237
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: EnumerateLoadedModulesEx, EnumerateLoadedModulesEx function, EnumerateLoadedModulesExW, base.enumerateloadedmodulesex, dbghelp/EnumerateLoadedModulesEx, dbghelp/EnumerateLoadedModulesExW
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
req.unicode-ansi: EnumerateLoadedModulesExW (Unicode) and EnumerateLoadedModulesEx (ANSI)
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
 - EnumerateLoadedModulesEx
 - EnumerateLoadedModulesEx
 - EnumerateLoadedModulesExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.8 or later
---

# EnumerateLoadedModulesExW function


## -description


Enumerates the loaded modules for the specified process.


## -parameters




### -param hProcess [in]

A handle to the process whose modules will be enumerated.


### -param EnumLoadedModulesCallback [in]

An application-defined callback function. For more information, see 
<a href="https://msdn.microsoft.com/f6acb9cf-81f7-4b05-95e2-9628855f6b51">EnumerateLoadedModulesProc64</a>.


### -param UserContext [in, optional]

Optional user-defined data. This value is passed to the callback function.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>
 

 

