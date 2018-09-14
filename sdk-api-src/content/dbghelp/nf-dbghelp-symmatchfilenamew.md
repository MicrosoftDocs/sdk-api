---
UID: NF:dbghelp.SymMatchFileNameW
title: SymMatchFileNameW function
author: windows-sdk-content
description: Compares a string to a file name and path.
old-location: base\symmatchfilename.htm
tech.root: Debug
ms.assetid: 69787cc7-db84-4c60-8d7d-f8eae18c82e9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SymMatchFileName, SymMatchFileName function, SymMatchFileNameW, _win32_symmatchfilename, base.symmatchfilename, dbghelp/SymMatchFileName, dbghelp/SymMatchFileNameW
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
req.unicode-ansi: SymMatchFileNameW (Unicode) and SymMatchFileName (ANSI)
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
 - SymMatchFileName
 - SymMatchFileName
 - SymMatchFileNameW
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
---

# SymMatchFileNameW function


## -description


Compares a string to a file name and path.


## -parameters




### -param FileName [in]

The file name to be compared to the <i>Match</i> parameter.


### -param Match [in]

The string to be compared to the <i>FileName</i> parameter.


### -param FileNameStop [out, optional]

A pointer to a string buffer that receives a pointer to the location in <i>FileName</i> where matching stopped. For a complete match, this value can be one character before <i>FileName</i>. This value can also be <b>NULL</b>.


### -param MatchStop [out, optional]

A pointer to a string buffer that receives a pointer to the location in <i>Match</i> where matching stopped. For a complete match, this value may be one character before <i>Match</i>. This value may be <b>NULL</b>.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Because the match string can be a suffix of the complete file name, this function can be used to match a plain file name to a fully qualified file name.

Matching begins from the end of both strings and proceeds backward. Matching is case-insensitive and equates a backslash ('\') with a forward slash ('/').

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>
 

 

