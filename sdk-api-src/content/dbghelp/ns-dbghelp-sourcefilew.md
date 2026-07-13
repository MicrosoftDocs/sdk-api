---
UID: NS:dbghelp._SOURCEFILEW
title: SOURCEFILEW (dbghelp.h)
description: The SOURCEFILEW (Unicode) structure (dbghelp.h) contains source file information.
helpviewer_keywords: ["*PSOURCEFILEW","PSOURCEFILE","PSOURCEFILE structure pointer","SOURCEFILE","SOURCEFILE structure","SOURCEFILEW","_SOURCEFILE","_SOURCEFILEW","base.sourcefile_str","dbghelp/PSOURCEFILE","dbghelp/SOURCEFILE","dbghelp/SOURCEFILEW"]
old-location: base\sourcefile_str.htm
tech.root: Debug
ms.assetid: b41b844d-85d2-4ea3-bdd9-1564898da9e1
ms.date: 08/04/2022
ms.keywords: '*PSOURCEFILEW, PSOURCEFILE, PSOURCEFILE structure pointer, SOURCEFILE, SOURCEFILE structure, SOURCEFILEW, _SOURCEFILE, _SOURCEFILEW, base.sourcefile_str, dbghelp/PSOURCEFILE, dbghelp/SOURCEFILE, dbghelp/SOURCEFILEW'
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
req.typenames: SOURCEFILEW, *PSOURCEFILEW
req.redist: DbgHelp.dll 6.3 or later
ms.custom: 19H1
f1_keywords:
 - _SOURCEFILEW
 - dbghelp/_SOURCEFILEW
 - PSOURCEFILEW
 - dbghelp/PSOURCEFILEW
 - SOURCEFILEW
 - dbghelp/SOURCEFILEW
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

# SOURCEFILEW structure


## -description

Contains source file information.

## -struct-fields

### -field ModBase

The base address of the module.

### -field FileName

The fully qualified source file name.

## -see-also

<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumsourcefiles">SymEnumSourceFiles</a>

## -remarks

> [!NOTE]
> The dbghelp.h header defines SOURCEFILE as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
