---
UID: NF:dbghelp.SymSetHomeDirectoryW
title: SymSetHomeDirectoryW function
author: windows-sdk-content
description: Sets the home directory used by Dbghelp.
old-location: base\symsethomedirectory.htm
old-project: debug
ms.assetid: 12e65054-c4d5-44b9-8597-b841cac012f5
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: SymSetHomeDirectory, SymSetHomeDirectory function, SymSetHomeDirectoryW, base.symsethomedirectory, dbghelp/SymSetHomeDirectory, dbghelp/SymSetHomeDirectoryW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.redist: DbgHelp.dll 6.1 or later
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymSetHomeDirectoryW (Unicode) and SymSetHomeDirectory (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IMAGEHLP_SYMBOL_TYPE_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
api_name:
 - SymSetHomeDirectory
 - SymSetHomeDirectory
 - SymSetHomeDirectoryW
product: Windows
targetos: Windows
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
---

# SymSetHomeDirectoryW function


## -description


Sets the home directory used by Dbghelp.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the <a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param dir [in, optional]

The home directory. This directory must be writable, otherwise the home directory is the common application directory specified with <a href="csidl_common_appdata">CSIDL_COMMON_APPDATA</a>. If this parameter is <b>NULL</b>, the function uses the default directory.


## -returns



If the function succeeds, the return value is a pointer to the <i>dir</i> parameter.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The default home directory is the directory in which Dbghelp.dll resides. Dbghelp uses this directory as a basis for other directories, such as the default downstream store directory (the sym subdirectory of the home directory).

The home directory used for the default symbol store and the source server cache location is stored in the DBGHELP_HOMEDIR environment variable.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/490de8cd-2738-4770-b708-fa2d61b83587">SymGetHomeDirectory</a>
 

 

