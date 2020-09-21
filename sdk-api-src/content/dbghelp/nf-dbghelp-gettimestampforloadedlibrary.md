---
UID: NF:dbghelp.GetTimestampForLoadedLibrary
title: GetTimestampForLoadedLibrary function (dbghelp.h)
description: Retrieves the time stamp of a loaded image.
helpviewer_keywords: ["GetTimestampForLoadedLibrary","GetTimestampForLoadedLibrary function","_win32_gettimestampforloadedlibrary","base.gettimestampforloadedlibrary","dbghelp/GetTimestampForLoadedLibrary"]
old-location: base\gettimestampforloadedlibrary.htm
tech.root: Debug
ms.assetid: 9ce7b211-5447-4624-b197-85730c4a7a10
ms.date: 12/05/2018
ms.keywords: GetTimestampForLoadedLibrary, GetTimestampForLoadedLibrary function, _win32_gettimestampforloadedlibrary, base.gettimestampforloadedlibrary, dbghelp/GetTimestampForLoadedLibrary
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
 - GetTimestampForLoadedLibrary
 - dbghelp/GetTimestampForLoadedLibrary
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
 - GetTimestampForLoadedLibrary
---

# GetTimestampForLoadedLibrary function


## -description

Retrieves the time stamp of a loaded image.

## -parameters

### -param Module [in]

The base address of an image that is mapped into memory by a call to the 
<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a> function.

## -returns

If the function succeeds, the return value is the time stamp from the image.

If the function fails, the return value is zero. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The time stamp for an image is initially set by the linker, but it can be modified by operations such as rebasing. The value is represented in the number of seconds elapsed since midnight (00:00:00), January 1, 1970, Universal Coordinated Time, according to the system clock. The time stamp can be printed using the C run-time (CRT) function ctime.

All <a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a>



<a href="/windows/desktop/api/imagehlp/nf-imagehlp-rebaseimage">ReBaseImage</a>



<a href="/windows/desktop/api/imagehlp/nf-imagehlp-rebaseimage64">ReBaseImage64</a>