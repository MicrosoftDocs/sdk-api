---
UID: NF:dbghelp.SymSrvGetFileIndexInfoW
title: SymSrvGetFileIndexInfoW function
author: windows-sdk-content
description: Retrieves the index information for the specified .pdb, .dbg, or image file.
old-location: base\symsrvgetfileindexinfo.htm
tech.root: debug
ms.assetid: ee5b0821-2746-467e-9d95-90776882ac95
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SymSrvGetFileIndexInfo, SymSrvGetFileIndexInfo function, SymSrvGetFileIndexInfoW, base.symsrvgetfileindexinfo, dbghelp/SymSrvGetFileIndexInfo, dbghelp/SymSrvGetFileIndexInfoW
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymSrvGetFileIndexInfoW (Unicode) and SymSrvGetFileIndexInfo (ANSI)
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
 - SymSrvGetFileIndexInfo
 - SymSrvGetFileIndexInfo
 - SymSrvGetFileIndexInfoW
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.6 or later
---

# SymSrvGetFileIndexInfoW function


## -description


Retrieves the index information for the specified .pdb, .dbg, or image file.


## -parameters




### -param File [in]

The name of the file.


### -param Info [out]

A <a href="https://msdn.microsoft.com/110cf21c-7768-48fd-bfdc-1f7cd30ca291">SYMSRV_INDEX_INFO</a> structure that receives the index information.


### -param Flags [in]

This parameter is reserved for future use.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.
						

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function is not for general use.  Those writing utilities for the management of files in symbol server stores may use to this function to predict the relative path the symbol server will look for a file.  It is used by srctool.exe to actually populate symbol server stores.  It may also be of use to those looking to find the parameters to feed the <a href="https://msdn.microsoft.com/f85d8cd9-958a-490a-b155-3a9abdeda922">SymFindFileInPath</a> function.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/110cf21c-7768-48fd-bfdc-1f7cd30ca291">SYMSRV_INDEX_INFO</a>
 

 

