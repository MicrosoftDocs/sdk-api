---
UID: NF:dbghelp.SymRefreshModuleList
title: SymRefreshModuleList function
author: windows-sdk-content
description: Refreshes the module list for the process.
old-location: base\symrefreshmodulelist.htm
tech.root: Debug
ms.assetid: c1c934e5-4a0a-4cb5-bb12-d6743f034ccb
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: SymRefreshModuleList, SymRefreshModuleList function, base.symrefreshmodulelist, dbghelp/SymRefreshModuleList
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
 - SymRefreshModuleList
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.5 or later
- apiref
: 
- 
: 
- SymRefreshModuleList
: 
---

# SymRefreshModuleList function


## -description


Refreshes the module list for the process.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.
						

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function enumerates the loaded modules for the process and effectively calls the 
<a href="https://msdn.microsoft.com/be50588b-066b-42ab-ba81-7537c811676f">SymLoadModule64</a> function for each module. This same process is performed by <a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> if <i>fInvadeProcess</i> is <b>TRUE</b>.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>
 

 

