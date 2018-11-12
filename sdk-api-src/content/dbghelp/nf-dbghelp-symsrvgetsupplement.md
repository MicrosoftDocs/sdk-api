---
UID: NF:dbghelp.SymSrvGetSupplement
title: SymSrvGetSupplement function
author: windows-sdk-content
description: Retrieves the specified file from the supplement for a symbol store.
old-location: base\symsrvgetsupplement.htm
tech.root: debug
ms.assetid: 2cad61c6-c8a1-437f-8e2c-1fa70eb348c2
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: SymSrvGetSupplement, SymSrvGetSupplement function, SymSrvGetSupplementW, base.symsrvgetsupplement, dbghelp/SymSrvGetSupplement, dbghelp/SymSrvGetSupplementW
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
req.unicode-ansi: SymSrvGetSupplementW (Unicode) and SymSrvGetSupplement (ANSI)
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
 - SymSrvGetSupplement
 - SymSrvGetSupplement
 - SymSrvGetSupplementW
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.3 or later
---

# SymSrvGetSupplement function


## -description


Retrieves the specified file from the supplement for a symbol store.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param SymPath [in, optional]

The symbol path. The function uses only the symbol stores described in standard syntax for symbol stores. All other paths are ignored. If this parameter is <b>NULL</b>, the function uses the symbol path set using the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> or <a href="https://msdn.microsoft.com/564ba1f6-65c6-4c45-bdbf-41ef0dd8a39d">SymSetSearchPath</a> function.


### -param Node [in]

The symbol file associated with the supplemental file.


### -param File [in]

The name of the file.


## -returns



If the function succeeds, the return value is the fully qualified path for the supplemental file.
						

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



For more information on supplemental files, see <a href="https://msdn.microsoft.com/579bd9ff-cb23-426b-8188-6897d83ada28">SymSrvStoreSupplement</a>.

This function returns a pointer to a buffer that may be reused by another function. Therefore, be sure to copy the data returned to another buffer immediately.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/579bd9ff-cb23-426b-8188-6897d83ada28">SymSrvStoreSupplement</a>
 

 

