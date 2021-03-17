---
UID: NF:dbghelp.UnmapDebugInformation
title: UnmapDebugInformation function (dbghelp.h)
description: Deallocates the memory and resources allocated by a call to the MapDebugInformation function.
helpviewer_keywords: ["UnmapDebugInformation","UnmapDebugInformation function","_win32_unmapdebuginformation","base.unmapdebuginformation","dbghelp/UnmapDebugInformation"]
old-location: base\unmapdebuginformation.htm
tech.root: Debug
ms.assetid: 86d82f23-7803-475f-8b23-c3964d33cb00
ms.date: 12/05/2018
ms.keywords: UnmapDebugInformation, UnmapDebugInformation function, _win32_unmapdebuginformation, base.unmapdebuginformation, dbghelp/UnmapDebugInformation
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
 - UnmapDebugInformation
 - dbghelp/UnmapDebugInformation
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
 - UnmapDebugInformation
---

# UnmapDebugInformation function


## -description

Deallocates the memory and resources allocated by a call to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-mapdebuginformation">MapDebugInformation</a> function.
<div class="alert"><b>Note</b>  This function is provided only for backward compatibility. New applications should use the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symunloadmodule">SymUnloadModule64</a> function.</div><div> </div>

## -parameters

### -param DebugInfo [in]

A pointer to an 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-image_debug_information">IMAGE_DEBUG_INFORMATION</a> structure that is returned from a call to 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-mapdebuginformation">MapDebugInformation</a>.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>UnmapDebugInformation</b> function is the counterpart to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-mapdebuginformation">MapDebugInformation</a> function and must be used to deallocate the memory and resources allocated by a call to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-mapdebuginformation">MapDebugInformation</a> function.
			

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-image_debug_information">IMAGE_DEBUG_INFORMATION</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-mapdebuginformation">MapDebugInformation</a>