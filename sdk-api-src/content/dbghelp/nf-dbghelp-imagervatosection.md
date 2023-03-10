---
UID: NF:dbghelp.ImageRvaToSection
title: ImageRvaToSection function (dbghelp.h)
description: Locates a relative virtual address (RVA) within the image header of a file that is mapped as a file and returns a pointer to the section table entry for that RVA.
helpviewer_keywords: ["ImageRvaToSection","ImageRvaToSection function","_win32_imagervatosection","base.imagervatosection","dbghelp/ImageRvaToSection"]
old-location: base\imagervatosection.htm
tech.root: Debug
ms.assetid: a11df748-242b-4dd8-bf57-7ac02548b701
ms.date: 12/05/2018
ms.keywords: ImageRvaToSection, ImageRvaToSection function, _win32_imagervatosection, base.imagervatosection, dbghelp/ImageRvaToSection
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
 - ImageRvaToSection
 - dbghelp/ImageRvaToSection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
api_name:
 - ImageRvaToSection
---

# ImageRvaToSection function


## -description

Locates a relative virtual address (RVA) within the image header of a file that is mapped as a file and returns a pointer to the section table entry for that RVA.

## -parameters

### -param NtHeaders [in]

A pointer to an 
<a href="/windows/win32/api/winnt/ns-winnt-image_nt_headers32">IMAGE_NT_HEADERS</a> structure. This structure can be obtained by calling the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-imagentheader">ImageNtHeader</a> function.

### -param Base [in]

This parameter is reserved.

### -param Rva [in]

The relative virtual address to be located.

## -returns

If the function succeeds, the return value is a pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-image_section_header">IMAGE_SECTION_HEADER</a> structure.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/win32/api/winnt/ns-winnt-image_nt_headers32">IMAGE_NT_HEADERS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-image_section_header">IMAGE_SECTION_HEADER</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-imagentheader">ImageNtHeader</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a>