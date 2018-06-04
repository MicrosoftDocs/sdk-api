---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# EnumDirTree function


## -description


Enumerates all occurrences of the specified file in the specified directory tree.


## -parameters




### -param hProcess [in, optional]

A handle to a process. This handle must have been previously passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param RootPath [in]

The path where the function should begin searching for the file.


### -param InputPathName [in]

The name of the file to be found. You can specify a partial path.


### -param OutputPathBuffer [out, optional]

A pointer to a buffer that receives the full path of the file. If the function fails or does not find a matching file, this buffer will still contain the last full path that was found. 

This parameter is optional and can be <b>NULL</b>.


### -param cb

TBD


### -param data

TBD




#### - Callback [in, optional]

An application-defined callback function, or <b>NULL</b>. For more information, see 
<a href="https://msdn.microsoft.com/eae41b83-bba5-4656-9a5c-b6ef56845954">EnumDirTreeProc</a>.


#### - CallbackData [in, optional]

The user-defined data or <b>NULL</b>. This value is passed to the callback function.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The search can be canceled if you register a 
<a href="https://msdn.microsoft.com/f3ba952b-ecc5-4235-a806-00c82d40e611">SymRegisterCallbackProc64</a> callback function. For every file operation, 
<i>EnumDirTree</i> calls this callback function with CBA_DEFERRED_SYMBOL_LOAD_CANCEL. If the callback function returns <b>TRUE</b>, 
<i>EnumDirTree</i> cancels the search.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/eae41b83-bba5-4656-9a5c-b6ef56845954">EnumDirTreeProc</a>
 

 

