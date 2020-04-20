---
UID: NF:dbghelp.ImageNtHeader
title: ImageNtHeader function (dbghelp.h)
description: Locates the IMAGE_NT_HEADERS structure in a PE image and returns a pointer to the data.helpviewer_keywords: ["ImageNtHeader","ImageNtHeader function","_win32_imagentheader","base.imagentheader","dbghelp/ImageNtHeader"]
old-location: base\imagentheader.htm
tech.root: Debug
ms.assetid: bf796c81-84d1-43e6-a2ff-b0be6f4603e0
ms.date: 12/05/2018
ms.keywords: ImageNtHeader, ImageNtHeader function, _win32_imagentheader, base.imagentheader, dbghelp/ImageNtHeader
f1_keywords:
- dbghelp/ImageNtHeader
dev_langs:
- c++
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
- emodel.dll
- imagehlp.dll
api_name:
- ImageNtHeader
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
---

# ImageNtHeader function


## -description


Locates the 
<a href="https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-image_nt_headers32">IMAGE_NT_HEADERS</a> structure in a PE image and returns a pointer to the data.


## -parameters




### -param Base [in]

The base address of an image that is mapped into memory by a call to the 
<a href="https://docs.microsoft.com/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a> function.


## -returns



If the function succeeds, the return value is a pointer to an 
<a href="https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-image_nt_headers32">IMAGE_NT_HEADERS</a> structure.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-image_nt_headers32">IMAGE_NT_HEADERS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a>
 

 

