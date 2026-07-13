---
UID: NF:libloaderapi.SizeofResource
title: SizeofResource function (libloaderapi.h)
description: Retrieves the size, in bytes, of the specified resource.
helpviewer_keywords: ["SizeofResource","SizeofResource function [Menus and Other Resources]","_win32_SizeofResource","_win32_sizeofresource_cpp","libloaderapi/SizeofResource","menurc.sizeofresource","winui._win32_sizeofresource"]
old-location: menurc\sizeofresource.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\sizeofresource.htm
ms.date: 12/05/2018
ms.keywords: SizeofResource, SizeofResource function [Menus and Other Resources], _win32_SizeofResource, _win32_sizeofresource_cpp, libloaderapi/SizeofResource, menurc.sizeofresource, winui._win32_sizeofresource
req.header: libloaderapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SizeofResource
 - libloaderapi/SizeofResource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-libraryloader-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-LibraryLoader-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-LibraryLoader-l1-1-1.dll
 - API-MS-Win-Core-LibraryLoader-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Libraryloader-l1-2-1.dll
 - API-MS-Win-Core-LibraryLoader-L1-2-2.dll
api_name:
 - SizeofResource
---

# SizeofResource function


## -description

Retrieves the size, in bytes, of the specified resource.

## -parameters

### -param hModule [in, optional]

Type: <b>HMODULE</b>

A handle to the module whose executable file contains the resource. Default is the module used to create the current process.

### -param hResInfo [in]

Type: <b>HRSRC</b>

A handle to the resource. This handle must be created by using the <a href="/windows/win32/api/winbase/nf-winbase-findresourcea">FindResource</a> or <a href="/windows/win32/api/winbase/nf-winbase-findresourceexa">FindResourceEx</a> function.

## -returns

Type: <b>DWORD</b>

If the function succeeds, the return value is the number of bytes in the resource.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/win32/api/winbase/nf-winbase-findresourcea">FindResource</a>



<a href="/windows/win32/api/winbase/nf-winbase-findresourceexa">FindResourceEx</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/ff321356-c999-4021-a537-fbe863996e24">Resources</a>
