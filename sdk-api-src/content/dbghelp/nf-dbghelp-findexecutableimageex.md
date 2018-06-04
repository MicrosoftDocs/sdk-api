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

# FindExecutableImageEx function


## -description


Locates the specified executable file.


## -parameters




### -param FileName [in]

The name of the symbol file to be located. This parameter can be a partial path.


### -param SymbolPath [in]

The path where symbol files are located. This string can contain multiple paths separated by semicolons. To retrieve the symbol path, use the 
<a href="https://msdn.microsoft.com/aa8c8450-ee67-4614-98a1-5feebdd3a788">SymGetSearchPath</a> function.


### -param ImageFilePath [out]

A pointer to a buffer that receives the full path of the executable file.


### -param Callback [in, optional]

An application-defined callback function that verifies whether the correct executable file was found, or whether the function should continue its search. For more information, see 
<a href="https://msdn.microsoft.com/cbd8cd63-8fdb-4314-8737-9f934de74f89">FindExecutableImageProc</a>. 




This parameter can be <b>NULL</b>.


### -param CallerData [in, optional]

Optional user-defined data for the callback function. This parameter can be <b>NULL</b>.


## -returns



If the function succeeds, the return value is an open handle to the executable file.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>FindExecutableImageEx</b> function is provided so executable files can be found in several different directories by using a single function call. If the <i>SymbolPath</i> parameter contains multiple paths, the function searches each specified directory tree for the executable file. When the file is found, the search stops. Thus, be sure to specify <i>SymbolPath</i> with the paths in the correct order.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/cbd8cd63-8fdb-4314-8737-9f934de74f89">FindExecutableImageProc</a>



<a href="https://msdn.microsoft.com/aa8c8450-ee67-4614-98a1-5feebdd3a788">SymGetSearchPath</a>
 

 

