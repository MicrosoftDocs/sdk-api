---
UID: NF:dbghelp.MapDebugInformation
title: MapDebugInformation function (dbghelp.h)
description: Obtains access to the debugging information for an image.
helpviewer_keywords: ["MapDebugInformation","MapDebugInformation function","_win32_mapdebuginformation","base.mapdebuginformation","dbghelp/MapDebugInformation"]
old-location: base\mapdebuginformation.htm
tech.root: Debug
ms.assetid: 749a2a99-f6c4-4af3-aa0b-8a7bb5c690da
ms.date: 12/05/2018
ms.keywords: MapDebugInformation, MapDebugInformation function, _win32_mapdebuginformation, base.mapdebuginformation, dbghelp/MapDebugInformation
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
 - MapDebugInformation
 - dbghelp/MapDebugInformation
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
 - MapDebugInformation
---

# MapDebugInformation function


## -description

Obtains access to the debugging information for an image.
<div class="alert"><b>Note</b>  This function is provided only for backward compatibility. It does not return reliable information. New applications should use the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetmoduleinfo">SymGetModuleInfo64</a> and 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symloadmodule">SymLoadModule64</a> functions. </div><div> </div>

## -parameters

### -param FileHandle [in, optional]

A handle to an open executable image or <b>NULL</b>.

### -param FileName [in]

The name of an executable image file or <b>NULL</b>.

### -param SymbolPath [in, optional]

The path where symbol files are located. The path can be multiple paths separated by semicolons. To retrieve the symbol path, use the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetsearchpath">SymGetSearchPath</a> function.

### -param ImageBase [in]

The base address for the image or zero.

## -returns

If the function succeeds, the return value is a pointer to an 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-image_debug_information">IMAGE_DEBUG_INFORMATION</a> structure.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>MapDebugInformation</b> function is used to obtain access to an image's debugging information. The debugging information is extracted from the image or the symbol file and placed into the 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-image_debug_information">IMAGE_DEBUG_INFORMATION</a> structure. This structure is allocated by the library and must be deallocated by using the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-unmapdebuginformation">UnmapDebugInformation</a> function. The memory for the structure is not in the process's default heap, so attempts to free it with a memory deallocation routine will fail.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-image_debug_information">IMAGE_DEBUG_INFORMATION</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetsearchpath">SymGetSearchPath</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-unmapdebuginformation">UnmapDebugInformation</a>