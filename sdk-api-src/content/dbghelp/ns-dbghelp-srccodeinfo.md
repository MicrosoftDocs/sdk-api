---
UID: NS:dbghelp._SRCCODEINFO
title: SRCCODEINFO (dbghelp.h)
description: The SRCCODEINFO structure (dbghelp.h) contains line information.
helpviewer_keywords: ["*PSRCCODEINFO","PSRCCODEINFO","PSRCCODEINFO structure pointer","SRCCODEINFO","SRCCODEINFO structure","SRCCODEINFOW","_SRCCODEINFO","_SRCCODEINFOW","base.srccodeinfo_str","dbghelp/PSRCCODEINFO","dbghelp/SRCCODEINFO","dbghelp/SRCCODEINFOW"]
old-location: base\srccodeinfo_str.htm
tech.root: Debug
ms.assetid: 8a2ee743-d2e8-402a-b659-0c0b75052d1d
ms.date: 08/04/2022
ms.keywords: '*PSRCCODEINFO, PSRCCODEINFO, PSRCCODEINFO structure pointer, SRCCODEINFO, SRCCODEINFO structure, SRCCODEINFOW, _SRCCODEINFO, _SRCCODEINFOW, base.srccodeinfo_str, dbghelp/PSRCCODEINFO, dbghelp/SRCCODEINFO, dbghelp/SRCCODEINFOW'
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SRCCODEINFOW (Unicode) and SRCCODEINFO (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SRCCODEINFO, *PSRCCODEINFO
req.redist: DbgHelp.dll 6.1 or later
ms.custom: 19H1
f1_keywords:
 - _SRCCODEINFO
 - dbghelp/_SRCCODEINFO
 - PSRCCODEINFO
 - dbghelp/PSRCCODEINFO
 - SRCCODEINFO
 - dbghelp/SRCCODEINFO
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
 - SRCCODEINFO
 - SRCCODEINFO
 - SRCCODEINFOW
---

# SRCCODEINFO structure


## -description

Contains line information.

## -struct-fields

### -field SizeOfStruct

The size of the structure, in bytes.

### -field Key

This member is not used.

### -field ModBase

The base address of the module that contains the line.

### -field Obj

The name of the object file within the module that contains the line.

### -field FileName

The fully qualified source file name.

### -field LineNumber

The line number within the source file.

### -field Address

The virtual address of the first instruction of the line.

## -see-also

<a href="/windows/desktop/api/dbghelp/nc-dbghelp-psym_enumlines_callback">SymEnumLinesProc</a>
