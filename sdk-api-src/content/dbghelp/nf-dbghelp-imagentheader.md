---
UID: NF:dbghelp.ImageNtHeader
title: ImageNtHeader function
author: windows-sdk-content
description: Locates the IMAGE_NT_HEADERS structure in a PE image and returns a pointer to the data.
old-location: base\imagentheader.htm
old-project: debug
ms.assetid: bf796c81-84d1-43e6-a2ff-b0be6f4603e0
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: ImageNtHeader, ImageNtHeader function, _win32_imagentheader, base.imagentheader, dbghelp/ImageNtHeader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.redist: DbgHelp.dll 5.1 or later
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
 - emodel.dll
 - imagehlp.dll
api_name:
 - ImageNtHeader
product: Windows
targetos: Windows
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
---

# ImageNtHeader function


## -description


Locates the 
<a href="https://msdn.microsoft.com/6511341f-252d-4f73-bb90-284bbb69b065">IMAGE_NT_HEADERS</a> structure in a PE image and returns a pointer to the data.


## -parameters




### -param Base [in]

The base address of an image that is mapped into memory by a call to the 
<a href="https://msdn.microsoft.com/df9f54cd-b2de-4107-a1c5-d5a07045851e">MapViewOfFile</a> function.


## -returns



If the function succeeds, the return value is a pointer to an 
<a href="https://msdn.microsoft.com/6511341f-252d-4f73-bb90-284bbb69b065">IMAGE_NT_HEADERS</a> structure.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/6511341f-252d-4f73-bb90-284bbb69b065">IMAGE_NT_HEADERS</a>



<a href="https://msdn.microsoft.com/df9f54cd-b2de-4107-a1c5-d5a07045851e">MapViewOfFile</a>
 

 

