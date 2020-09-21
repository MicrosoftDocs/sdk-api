---
UID: NF:dbghelp.SymGetOmaps
title: SymGetOmaps function (dbghelp.h)
description: Retrieves the omap tables within a loaded module.
helpviewer_keywords: ["SymGetOmaps","SymGetOmaps function","base.symgetomaps","dbghelp/SymGetOmaps"]
old-location: base\symgetomaps.htm
tech.root: Debug
ms.assetid: d89947fa-65fd-4929-9f7e-a4923792049e
ms.date: 12/05/2018
ms.keywords: SymGetOmaps, SymGetOmaps function, base.symgetomaps, dbghelp/SymGetOmaps
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
req.redist: DbgHelp.dll 6.8 or later
ms.custom: 19H1
f1_keywords:
 - SymGetOmaps
 - dbghelp/SymGetOmaps
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
 - SymGetOmaps
---

# SymGetOmaps function


## -description

Retrieves the omap tables within a loaded module.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param BaseOfDll [in]

The base address of the module.

### -param OmapTo [out]

An array of address map entries to the new image layout taken from the original layout. For details on the map entries, see the <a href="/windows/desktop/api/dbghelp/ns-dbghelp-omap">OMAP</a> structure.

### -param cOmapTo [out]

The number of entries in the <i>OmapTo</i> array.

### -param OmapFrom [out]

An array of address map entries from the new image layout to the original layout (as described by the debug symbols). For details on the map entries, see the <a href="/windows/desktop/api/dbghelp/ns-dbghelp-omap">OMAP</a> structure.

### -param cOmapFrom [out]

The number of entries in the <i>OmapFrom</i> array.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails (the omap is not found), the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/api/dbghelp/ns-dbghelp-omap">OMAP</a>