---
UID: NF:dbghelp.ImageRvaToVa
title: ImageRvaToVa function (dbghelp.h)
description: Locates a relative virtual address (RVA) within the image header of a file that is mapped as a file and returns the virtual address of the corresponding byte in the file.
helpviewer_keywords: ["ImageRvaToVa","ImageRvaToVa function","_win32_imagervatova","base.imagervatova","dbghelp/ImageRvaToVa"]
old-location: base\imagervatova.htm
tech.root: Debug
ms.assetid: 7f022054-d98e-44c8-b256-5c34711ce471
ms.date: 12/05/2018
ms.keywords: ImageRvaToVa, ImageRvaToVa function, _win32_imagervatova, base.imagervatova, dbghelp/ImageRvaToVa
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
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - ImageRvaToVa
 - dbghelp/ImageRvaToVa
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
 - imagehlp.dll
api_name:
 - ImageRvaToVa
---

# ImageRvaToVa function


## -description

Locates a relative virtual address (RVA) within the image header of a file that is mapped as a file and returns the virtual address of the corresponding byte in the file.

## -parameters

### -param NtHeaders [in]

A pointer to an 
<a href="/windows/win32/api/winnt/ns-winnt-image_nt_headers32">IMAGE_NT_HEADERS</a> structure. This structure can be obtained by calling the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-imagentheader">ImageNtHeader</a> function.

### -param Base [in]

The base address of an image that is mapped into memory through a call to the 
<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a> function.

### -param Rva [in]

The relative virtual address to be located.

### -param LastRvaSection [in, optional]

A pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-image_section_header">IMAGE_SECTION_HEADER</a> structure that specifies the last RVA section. This is an optional parameter. When specified, it points to a variable that contains the last section value used for the specified image to translate an RVA to a VA.

## -returns

If the function succeeds, the return value is the virtual address in the mapped file.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>ImageRvaToVa</b> function locates an RVA within the image header of a file that is mapped as a file and returns the virtual address of the corresponding byte in the file.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/win32/api/winnt/ns-winnt-image_nt_headers32">IMAGE_NT_HEADERS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-image_section_header">IMAGE_SECTION_HEADER</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-imagentheader">ImageNtHeader</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a>