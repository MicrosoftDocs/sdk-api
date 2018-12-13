---
UID: NF:dbghelp.FindDebugInfoFileExW
title: FindDebugInfoFileExW function
author: windows-sdk-content
description: Locates the specified debug (.dbg) file.
old-location: base\finddebuginfofileex.htm
tech.root: debug
ms.assetid: 1e89fe9a-4631-42b9-96ee-90393b4d9084
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FindDebugInfoFileEx, FindDebugInfoFileEx function, FindDebugInfoFileExW, _win32_finddebuginfofileex, base.finddebuginfofileex, dbghelp/FindDebugInfoFileEx, dbghelp/FindDebugInfoFileExW
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
req.unicode-ansi: FindDebugInfoFileExW (Unicode) and FindDebugInfoFileEx (ANSI)
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
 - FindDebugInfoFileEx
 - FindDebugInfoFileEx
 - FindDebugInfoFileExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
---

# FindDebugInfoFileExW function


## -description


Locates the specified 
<a href="https://msdn.microsoft.com/610e5cd3-9dc3-462c-98f8-6a63874464f8">debug (.dbg) file</a>.


## -parameters




### -param FileName [in]

The name of the .dbg file to locate. You can use a partial path.


### -param SymbolPath [in]

The path where symbol files are located. This can be multiple paths separated by semicolons. To retrieve the symbol path, use the 
<a href="https://msdn.microsoft.com/aa8c8450-ee67-4614-98a1-5feebdd3a788">SymGetSearchPath</a> function.


### -param DebugFilePath [out]

A pointer to a buffer that receives the full path of the .dbg file.


### -param Callback [in, optional]

An application-defined callback function that verifies whether the correct file was found or the function should continue its search. For more information, see 
<a href="https://msdn.microsoft.com/c7ccc66a-7897-4430-8874-a4ba66a5cce7">FindDebugInfoFileProc</a>. 




This parameter may be <b>NULL</b>.


### -param CallerData [in, optional]

Optional user-defined data to pass to the callback function.


## -returns



If the function succeeds, the return value is an open handle to the .dbg file.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>FindDebugInfoFileEx</b> function is used to locate a .dbg file. This function is provided so the search can be conducted in several different directories through a single function call. The <i>SymbolPath</i> parameter can contain multiple paths, with each separated by a semicolon (;). When multiple paths are specified, the function searches each specified directory for the file. When the file is located, the search stops. Thus, be sure to specify <i>SymbolPath</i> with the paths in the correct order.

If the file name specified does not include a .dbg extension, 
<b>FindDebugInfoFileEx</b> searches for the file in the following sequence:

<ol>
<li><i>SymbolPath</i>\Symbols\<i>ext</i>\<i>filename</i>.dbg</li>
<li><i>SymbolPath</i>\<i>ext</i>\<i>filename</i>.dbg</li>
<li><i>SymbolPath</i>\<i>filename</i>.dbg</li>
<li><i>FileNamePath</i>\<i>filename</i>.dbg</li>
</ol>
All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/c7ccc66a-7897-4430-8874-a4ba66a5cce7">FindDebugInfoFileProc</a>



<a href="https://msdn.microsoft.com/aa8c8450-ee67-4614-98a1-5feebdd3a788">SymGetSearchPath</a>
 

 

