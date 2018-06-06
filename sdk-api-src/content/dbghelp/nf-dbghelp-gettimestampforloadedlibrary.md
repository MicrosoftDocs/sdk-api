---
UID: NF:dbghelp.GetTimestampForLoadedLibrary
title: GetTimestampForLoadedLibrary function
author: windows-sdk-content
description: Retrieves the time stamp of a loaded image.
old-location: base\gettimestampforloadedlibrary.htm
old-project: Debug
ms.assetid: 9ce7b211-5447-4624-b197-85730c4a7a10
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: GetTimestampForLoadedLibrary, GetTimestampForLoadedLibrary function, _win32_gettimestampforloadedlibrary, base.gettimestampforloadedlibrary, dbghelp/GetTimestampForLoadedLibrary
ms.prod: windows
ms.technology: windows-sdk
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
 - GetTimestampForLoadedLibrary
product: Windows
targetos: Windows
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
---

# GetTimestampForLoadedLibrary function


## -description


Retrieves the time stamp of a loaded image.


## -parameters




### -param Module

TBD




#### - ImageBase [in]

The base address of an image that is mapped into memory by a call to the 
<a href="https://msdn.microsoft.com/df9f54cd-b2de-4107-a1c5-d5a07045851e">MapViewOfFile</a> function.


## -returns



If the function succeeds, the return value is the time stamp from the image.

If the function fails, the return value is zero. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The time stamp for an image is initially set by the linker, but it can be modified by operations such as rebasing. The value is represented in the number of seconds elapsed since midnight (00:00:00), January 1, 1970, Universal Coordinated Time, according to the system clock. The time stamp can be printed using the C run-time (CRT) function ctime.

All <a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/df9f54cd-b2de-4107-a1c5-d5a07045851e">MapViewOfFile</a>



<a href="https://msdn.microsoft.com/b17eb5e6-38de-4baf-a958-189d8c4454af">ReBaseImage</a>



<a href="https://msdn.microsoft.com/3d60358c-8aa6-4b30-a46e-ce0e15964b5a">ReBaseImage64</a>
 

 

