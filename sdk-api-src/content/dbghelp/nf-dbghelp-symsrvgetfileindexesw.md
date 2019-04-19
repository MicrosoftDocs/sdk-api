---
UID: NF:dbghelp.SymSrvGetFileIndexesW
title: SymSrvGetFileIndexesW function (dbghelp.h)
author: windows-sdk-content
description: Retrieves the indexes for the specified .pdb, .dbg, or image file that would be used to store the file. The combination of these values uniquely identifies the file in the symbol server.
old-location: base\symsrvgetfileindexes.htm
tech.root: Debug
ms.assetid: 9a6c6949-1ba2-4ed9-a038-68c57560454a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SymSrvGetFileIndexes, SymSrvGetFileIndexes function, SymSrvGetFileIndexesW, base.symsrvgetfileindexes, dbghelp/SymSrvGetFileIndexes, dbghelp/SymSrvGetFileIndexesW
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymSrvGetFileIndexesW (Unicode) and SymSrvGetFileIndexes (ANSI)
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
 - SymSrvGetFileIndexes
 - SymSrvGetFileIndexes
 - SymSrvGetFileIndexesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.3 or later
ms.custom: 19H1
---

# SymSrvGetFileIndexesW function


## -description


Retrieves the indexes for the specified .pdb, .dbg, or image file that would be used to store the file. The combination of these values uniquely identifies the file in the symbol server. They can be used when calling the <a href="https://msdn.microsoft.com/f85d8cd9-958a-490a-b155-3a9abdeda922">SymFindFileInPath</a> function to search for a file in a symbol store.


## -parameters




### -param File [in]

The name of the file.


### -param Id [out]

The first of three identifying parameters.


### -param Val1 [out]

The second of three identifying parameters.


### -param Val2 [out, optional]

The third of three identifying parameters.


### -param Flags [in]

This parameter is reserved for future use.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>
 

 

