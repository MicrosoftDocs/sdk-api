---
UID: NF:dbghelp.ImageRvaToVa
title: ImageRvaToVa function
author: windows-sdk-content
description: Locates a relative virtual address (RVA) within the image header of a file that is mapped as a file and returns the virtual address of the corresponding byte in the file.
old-location: base\imagervatova.htm
old-project: Debug
ms.assetid: 7f022054-d98e-44c8-b256-5c34711ce471
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: ImageRvaToVa, ImageRvaToVa function, _win32_imagervatova, base.imagervatova, dbghelp/ImageRvaToVa
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dbghelp.dll
-	imagehlp.dll
api_name:
-	ImageRvaToVa
product: Windows
targetos: Windows
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
---

# ImageRvaToVa function


## -description


Locates a relative virtual address (RVA) within the image header of a file that is mapped as a file and returns the virtual address of the corresponding byte in the file.


## -parameters




### -param NtHeaders [in]

A pointer to an 
<a href="https://msdn.microsoft.com/6511341f-252d-4f73-bb90-284bbb69b065">IMAGE_NT_HEADERS</a> structure. This structure can be obtained by calling the 
<a href="https://msdn.microsoft.com/bf796c81-84d1-43e6-a2ff-b0be6f4603e0">ImageNtHeader</a> function.


### -param Base [in]

The base address of an image that is mapped into memory through a call to the 
<a href="https://msdn.microsoft.com/df9f54cd-b2de-4107-a1c5-d5a07045851e">MapViewOfFile</a> function.


### -param Rva [in]

The relative virtual address to be located.


### -param LastRvaSection [in, optional]

A pointer to an 
<a href="https://msdn.microsoft.com/81ddf56d-66cc-4a0c-9cff-a84376a3223d">IMAGE_SECTION_HEADER</a> structure that specifies the last RVA section. This is an optional parameter. When specified, it points to a variable that contains the last section value used for the specified image to translate an RVA to a VA.


## -returns



If the function succeeds, the return value is the virtual address in the mapped file.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>ImageRvaToVa</b> function locates an RVA within the image header of a file that is mapped as a file and returns the virtual address of the corresponding byte in the file.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/6511341f-252d-4f73-bb90-284bbb69b065">IMAGE_NT_HEADERS</a>



<a href="https://msdn.microsoft.com/81ddf56d-66cc-4a0c-9cff-a84376a3223d">IMAGE_SECTION_HEADER</a>



<a href="https://msdn.microsoft.com/bf796c81-84d1-43e6-a2ff-b0be6f4603e0">ImageNtHeader</a>



<a href="https://msdn.microsoft.com/df9f54cd-b2de-4107-a1c5-d5a07045851e">MapViewOfFile</a>
 

 

