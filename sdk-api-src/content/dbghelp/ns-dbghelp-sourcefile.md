---
UID: NS:dbghelp._SOURCEFILE
title: SOURCEFILE (dbghelp.h)
description: The SOURCEFILE structure (dbghelp.h) contains source file information.
helpviewer_keywords: ["*PSOURCEFILE","PSOURCEFILE","PSOURCEFILE structure pointer","SOURCEFILE","SOURCEFILE structure","SOURCEFILEW","_SOURCEFILE","_SOURCEFILEW","base.sourcefile_str","dbghelp/PSOURCEFILE","dbghelp/SOURCEFILE","dbghelp/SOURCEFILEW"]
old-location: base\sourcefile_str.htm
tech.root: Debug
ms.assetid: b41b844d-85d2-4ea3-bdd9-1564898da9e1
ms.date: 08/04/2022
ms.keywords: '*PSOURCEFILE, PSOURCEFILE, PSOURCEFILE structure pointer, SOURCEFILE, SOURCEFILE structure, SOURCEFILEW, _SOURCEFILE, _SOURCEFILEW, base.sourcefile_str, dbghelp/PSOURCEFILE, dbghelp/SOURCEFILE, dbghelp/SOURCEFILEW'
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SOURCEFILEW (Unicode) and SOURCEFILE (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SOURCEFILE, *PSOURCEFILE
req.redist: DbgHelp.dll 6.3 or later
ms.custom: 19H1
f1_keywords:
 - _SOURCEFILE
 - dbghelp/_SOURCEFILE
 - PSOURCEFILE
 - dbghelp/PSOURCEFILE
 - SOURCEFILE
 - dbghelp/SOURCEFILE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DbgHelp.h
api_name:
 - SOURCEFILE
 - SOURCEFILE
 - SOURCEFILEW
---

# SOURCEFILE structure


## -description

Contains source file information.

## -struct-fields

### -field ModBase

The base address of the module.

### -field FileName

The fully qualified source file name.

## -see-also

<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumsourcefiles">SymEnumSourceFiles</a>
