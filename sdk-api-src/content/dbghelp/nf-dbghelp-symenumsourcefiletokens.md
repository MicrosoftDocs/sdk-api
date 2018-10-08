---
UID: NF:dbghelp.SymEnumSourceFileTokens
title: SymEnumSourceFileTokens function
author: windows-sdk-content
description: Enumerates all individual entries in a module's source server data, if available.
old-location: base\symenumsourcefiletokens.htm
tech.root: debug
ms.assetid: 0377ef07-bf9f-4938-8fc4-ae14373db590
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: SymEnumSourceFileTokens, SymEnumSourceFileTokens function, base.symenumsourcefiletokens, dbghelp/SymEnumSourceFileTokens
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
 - SymEnumSourceFileTokens
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.8 or later
---

# SymEnumSourceFileTokens function


## -description


Enumerates all individual entries in a module's <a href="https://msdn.microsoft.com/c7bf51ce-7fb4-49aa-ad33-e551b2c8362b">source server</a> data, if available.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param Base [in]

The base address of the module.


### -param Callback [in]

A 
<a href="https://msdn.microsoft.com/20c0eb1e-671b-4d31-88d4-57f2c149fcd9">SymEnumSourceFileTokensProc</a> callback function that receives the symbol information.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Some modules have PDB files with <a href="https://msdn.microsoft.com/c7bf51ce-7fb4-49aa-ad33-e551b2c8362b">source server</a> information detailing the version control information for each of the source files used to create each individual module.  An application can use this function to enumerate the  data for every source file that was "source indexed".

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/c7bf51ce-7fb4-49aa-ad33-e551b2c8362b">Source Server</a>



<a href="https://msdn.microsoft.com/20c0eb1e-671b-4d31-88d4-57f2c149fcd9">SymEnumSourceFileTokensProc</a>
 

 

