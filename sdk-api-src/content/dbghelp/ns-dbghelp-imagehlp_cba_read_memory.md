---
UID: NS:dbghelp._IMAGEHLP_CBA_READ_MEMORY
title: IMAGEHLP_CBA_READ_MEMORY (dbghelp.h)
description: Contains information about a memory read operation.
helpviewer_keywords: ["*PIMAGEHLP_CBA_READ_MEMORY","IMAGEHLP_CBA_READ_MEMORY","IMAGEHLP_CBA_READ_MEMORY structure","PIMAGEHLP_CBA_READ_MEMORY","PIMAGEHLP_CBA_READ_MEMORY structure pointer","_IMAGEHLP_CBA_READ_MEMORY","_win32_imagehlp_cba_read_memory_str","base.imagehlp_cba_read_memory_str","dbghelp/IMAGEHLP_CBA_READ_MEMORY","dbghelp/PIMAGEHLP_CBA_READ_MEMORY"]
old-location: base\imagehlp_cba_read_memory_str.htm
tech.root: Debug
ms.assetid: c5115fdc-aca6-4293-9c2b-82fd64ec7cb6
ms.date: 12/05/2018
ms.keywords: '*PIMAGEHLP_CBA_READ_MEMORY, IMAGEHLP_CBA_READ_MEMORY, IMAGEHLP_CBA_READ_MEMORY structure, PIMAGEHLP_CBA_READ_MEMORY, PIMAGEHLP_CBA_READ_MEMORY structure pointer, _IMAGEHLP_CBA_READ_MEMORY, _win32_imagehlp_cba_read_memory_str, base.imagehlp_cba_read_memory_str, dbghelp/IMAGEHLP_CBA_READ_MEMORY, dbghelp/PIMAGEHLP_CBA_READ_MEMORY'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IMAGEHLP_CBA_READ_MEMORY, *PIMAGEHLP_CBA_READ_MEMORY
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _IMAGEHLP_CBA_READ_MEMORY
 - dbghelp/_IMAGEHLP_CBA_READ_MEMORY
 - PIMAGEHLP_CBA_READ_MEMORY
 - dbghelp/PIMAGEHLP_CBA_READ_MEMORY
 - IMAGEHLP_CBA_READ_MEMORY
 - dbghelp/IMAGEHLP_CBA_READ_MEMORY
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
 - IMAGEHLP_CBA_READ_MEMORY
---

# IMAGEHLP_CBA_READ_MEMORY structure


## -description

Contains information about a memory read operation.

## -struct-fields

### -field addr

The address to be read.

### -field buf

A pointer to a buffer that receives the memory read.

### -field bytes

The number of bytes to read.

### -field bytesread

A pointer to a variable that receives the number of bytes read.

## -see-also

<a href="/windows/desktop/api/dbghelp/nc-dbghelp-psymbol_registered_callback">SymRegisterCallbackProc64</a>