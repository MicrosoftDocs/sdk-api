---
UID: NF:dbghelp.SymSrvGetFileIndexString
title: SymSrvGetFileIndexString function (dbghelp.h)
author: windows-sdk-content
description: Retrieves the index string for the specified .pdb, .dbg, or image file.
old-location: base\symsrvgetfileindexstring.htm
tech.root: Debug
ms.assetid: e66598fb-d7c7-4fde-a995-bfd1e7ceb24b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SymSrvGetFileIndexString, SymSrvGetFileIndexString function, SymSrvGetFileIndexStringW, base.symsrvgetfileindexstring, dbghelp/SymSrvGetFileIndexString, dbghelp/SymSrvGetFileIndexStringW
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymSrvGetFileIndexStringW (Unicode) and SymSrvGetFileIndexString (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DbgHelp.lib
req.dll: DbgHelp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - DbgHelp.dll
api_name:
 - SymSrvGetFileIndexString
 - SymSrvGetFileIndexString
 - SymSrvGetFileIndexStringW
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.3 or later
---

# SymSrvGetFileIndexString function


## -description


Retrieves the index string for the specified .pdb, .dbg, or image file.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param SrvPath [in, optional]

The path to the symbol server.


### -param File [in]

The name of the file.


### -param Index [out]

A pointer to a 
buffer that receives the index string.


### -param Size [in]

The size of 
the <i>Index</i> buffer, in characters.


### -param Flags [in]

This parameter is reserved for future use.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.
						

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function is not for general use.  Those writing utilities for the management of files in symbol server stores may use to this function to predict the relative path the symbol server will look for a file.  It is used by srctool.exe to actually populate symbol server stores.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>
 

 

