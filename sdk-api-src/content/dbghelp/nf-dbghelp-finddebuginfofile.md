---
UID: NF:dbghelp.FindDebugInfoFile
title: FindDebugInfoFile function
author: windows-driver-content
description: Locates a debug (.dbg) file.
old-location: base\finddebuginfofile.htm
old-project: Debug
ms.assetid: a13d3bf4-f34d-4304-9d47-aa21c3fa23b8
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: FindDebugInfoFile, FindDebugInfoFile function, _win32_finddebuginfofile, base.finddebuginfofile, dbghelp/FindDebugInfoFile
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
req.typenames: IMAGEHLP_SYMBOL_TYPE_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dbghelp.dll
api_name:
-	FindDebugInfoFile
product: Windows
targetos: Windows
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
---

# FindDebugInfoFile function


## -description


Locates a 
<a href="https://msdn.microsoft.com/610e5cd3-9dc3-462c-98f8-6a63874464f8">debug (.dbg) file</a>.

To provide a callback function to verify the symbol file located, use the 
<a href="https://msdn.microsoft.com/1e89fe9a-4631-42b9-96ee-90393b4d9084">FindDebugInfoFileEx</a> function.


## -parameters




### -param FileName [in]

The name of the .dbg file that is desired. You can use a partial path.


### -param SymbolPath [in]

The path where symbol files are located. This can be multiple paths separated by semicolons. To retrieve the symbol path, use the 
<a href="https://msdn.microsoft.com/aa8c8450-ee67-4614-98a1-5feebdd3a788">SymGetSearchPath</a> function.


### -param DebugFilePath [out]

A pointer to a buffer that receives the full path of the .dbg file.


## -returns



If the function succeeds, the return value is an open handle to the .dbg file.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>FindDebugInfoFile</b> function is used to locate a .dbg file. This function is provided so the search can be conducted in several different directories through a single function call. The <i>SymbolPath</i> parameter can contain multiple paths, with each separated by a semicolon (;). When multiple paths are specified, the function searches each directory for the file. Subdirectories are not searched. When the file is located, the search stops. Thus, be sure to specify <i>SymbolPath</i> with the paths in the correct order.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/1e89fe9a-4631-42b9-96ee-90393b4d9084">FindDebugInfoFileEx</a>



<a href="https://msdn.microsoft.com/aa8c8450-ee67-4614-98a1-5feebdd3a788">SymGetSearchPath</a>
 

 

