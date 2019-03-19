---
UID: NF:dbghelp.ImageRvaToSection
title: ImageRvaToSection function (dbghelp.h)
author: windows-sdk-content
description: Locates a relative virtual address (RVA) within the image header of a file that is mapped as a file and returns a pointer to the section table entry for that RVA.
old-location: base\imagervatosection.htm
tech.root: Debug
ms.assetid: a11df748-242b-4dd8-bf57-7ac02548b701
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ImageRvaToSection, ImageRvaToSection function, _win32_imagervatosection, base.imagervatosection, dbghelp/ImageRvaToSection
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
 - ImageRvaToSection
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
---

# ImageRvaToSection function


## -description


Locates a relative virtual address (RVA) within the image header of a file that is mapped as a file and returns a pointer to the section table entry for that RVA.


## -parameters




### -param NtHeaders [in]

A pointer to an 
<a href="https://msdn.microsoft.com/6511341f-252d-4f73-bb90-284bbb69b065">IMAGE_NT_HEADERS</a> structure. This structure can be obtained by calling the 
<a href="https://msdn.microsoft.com/bf796c81-84d1-43e6-a2ff-b0be6f4603e0">ImageNtHeader</a> function.


### -param Base [in]

This parameter is reserved.


### -param Rva [in]

The relative virtual address to be located.


## -returns



If the function succeeds, the return value is a pointer to an 
<a href="https://msdn.microsoft.com/81ddf56d-66cc-4a0c-9cff-a84376a3223d">IMAGE_SECTION_HEADER</a> structure.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/6511341f-252d-4f73-bb90-284bbb69b065">IMAGE_NT_HEADERS</a>



<a href="https://msdn.microsoft.com/81ddf56d-66cc-4a0c-9cff-a84376a3223d">IMAGE_SECTION_HEADER</a>



<a href="https://msdn.microsoft.com/bf796c81-84d1-43e6-a2ff-b0be6f4603e0">ImageNtHeader</a>



<a href="https://msdn.microsoft.com/df9f54cd-b2de-4107-a1c5-d5a07045851e">MapViewOfFile</a>
 

 

