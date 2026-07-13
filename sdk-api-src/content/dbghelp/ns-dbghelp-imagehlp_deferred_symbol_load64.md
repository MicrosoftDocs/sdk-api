---
UID: NS:dbghelp._IMAGEHLP_DEFERRED_SYMBOL_LOAD64
title: IMAGEHLP_DEFERRED_SYMBOL_LOAD64 (dbghelp.h)
description: Contains information about a deferred symbol load. (IMAGEHLP_DEFERRED_SYMBOL_LOAD64)
helpviewer_keywords: ["*PIMAGEHLP_DEFERRED_SYMBOL_LOAD64","DSLFLAG_MISMATCHED_DBG","DSLFLAG_MISMATCHED_PDB","IMAGEHLP_DEFERRED_SYMBOL_LOAD","IMAGEHLP_DEFERRED_SYMBOL_LOAD structure","IMAGEHLP_DEFERRED_SYMBOL_LOAD64","IMAGEHLP_DEFERRED_SYMBOL_LOAD64 structure","IMAGEHLP_DEFERRED_SYMBOL_LOADW64","PIMAGEHLP_DEFERRED_SYMBOL_LOAD64","PIMAGEHLP_DEFERRED_SYMBOL_LOAD64 structure pointer","_IMAGEHLP_DEFERRED_SYMBOL_LOAD64","_win32_imagehlp_deferred_symbol_load64_str","base.imagehlp_deferred_symbol_load64_str","dbghelp/IMAGEHLP_DEFERRED_SYMBOL_LOAD64","dbghelp/IMAGEHLP_DEFERRED_SYMBOL_LOADW64","dbghelp/PIMAGEHLP_DEFERRED_SYMBOL_LOAD64"]
old-location: base\imagehlp_deferred_symbol_load64_str.htm
tech.root: Debug
ms.assetid: 151c47dd-df4a-44c9-ad9f-1ffc80dd81e9
ms.date: 12/05/2018
ms.keywords: '*PIMAGEHLP_DEFERRED_SYMBOL_LOAD64, DSLFLAG_MISMATCHED_DBG, DSLFLAG_MISMATCHED_PDB, IMAGEHLP_DEFERRED_SYMBOL_LOAD, IMAGEHLP_DEFERRED_SYMBOL_LOAD structure, IMAGEHLP_DEFERRED_SYMBOL_LOAD64, IMAGEHLP_DEFERRED_SYMBOL_LOAD64 structure, IMAGEHLP_DEFERRED_SYMBOL_LOADW64, PIMAGEHLP_DEFERRED_SYMBOL_LOAD64, PIMAGEHLP_DEFERRED_SYMBOL_LOAD64 structure pointer, _IMAGEHLP_DEFERRED_SYMBOL_LOAD64, _win32_imagehlp_deferred_symbol_load64_str, base.imagehlp_deferred_symbol_load64_str, dbghelp/IMAGEHLP_DEFERRED_SYMBOL_LOAD64, dbghelp/IMAGEHLP_DEFERRED_SYMBOL_LOADW64, dbghelp/PIMAGEHLP_DEFERRED_SYMBOL_LOAD64'
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: IMAGEHLP_DEFERRED_SYMBOL_LOADW64 (Unicode) and IMAGEHLP_DEFERRED_SYMBOL_LOAD64 (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IMAGEHLP_DEFERRED_SYMBOL_LOAD64, *PIMAGEHLP_DEFERRED_SYMBOL_LOAD64
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _IMAGEHLP_DEFERRED_SYMBOL_LOAD64
 - dbghelp/_IMAGEHLP_DEFERRED_SYMBOL_LOAD64
 - PIMAGEHLP_DEFERRED_SYMBOL_LOAD64
 - dbghelp/PIMAGEHLP_DEFERRED_SYMBOL_LOAD64
 - IMAGEHLP_DEFERRED_SYMBOL_LOAD64
 - dbghelp/IMAGEHLP_DEFERRED_SYMBOL_LOAD64
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
 - IMAGEHLP_DEFERRED_SYMBOL_LOAD64
 - IMAGEHLP_DEFERRED_SYMBOL_LOAD64
 - IMAGEHLP_DEFERRED_SYMBOL_LOADW64
 - IMAGEHLP_DEFERRED_SYMBOL_LOAD
---

## -description

Contains information about a deferred symbol load.

## -struct-fields

### -field SizeOfStruct

The size of the structure, in bytes. The caller must set this member to <code>sizeof(IMAGEHLP_DEFERRED_SYMBOL_LOAD64)</code>.

### -field BaseOfImage

The base virtual address where the image is loaded.

### -field CheckSum

The computed checksum of the image. This value can be zero.

### -field TimeDateStamp

The date and timestamp value. The value is represented in the number of seconds elapsed since midnight (00:00:00), January 1, 1970, Universal Coordinated Time, according to the system clock. The timestamp can be printed using the C run-time (CRT) function <b>ctime</b>.

### -field FileName

The image name. The name may or may not contain a full path.

### -field Reparse

If this member is <b>TRUE</b>, the operation should be performed again. Otherwise, it should not.

### -field hFile

A handle to a file. This member is used with <b>CBA_DEFERRED_SYMBOL_LOAD_PARTIAL</b> and <b>IMAGEHLP_DEFERRED_SYMBOL_LOAD_FAILURE</b> callbacks.

### -field Flags

This member can be one of the following values.

- DSLFLAG_MISMATCHED_DBG (0x2)
- DSLFLAG_MISMATCHED_PDB (0x1)

## -remarks

This structure supersedes the <b>IMAGEHLP_DEFERRED_SYMBOL_LOAD</b> structure. For more information, see 
<a href="/windows/desktop/Debug/updated-platform-support">Updated Platform Support</a>. <b>IMAGEHLP_DEFERRED_SYMBOL_LOAD</b> is defined as follows in DbgHelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define IMAGEHLP_DEFERRED_SYMBOL_LOAD IMAGEHLP_DEFERRED_SYMBOL_LOAD64
#define PIMAGEHLP_DEFERRED_SYMBOL_LOAD PIMAGEHLP_DEFERRED_SYMBOL_LOAD64
#else
typedef struct _IMAGEHLP_DEFERRED_SYMBOL_LOAD {
    DWORD    SizeOfStruct; 
    DWORD    BaseOfImage;  
    DWORD    CheckSum; 
    DWORD    TimeDateStamp; 
    CHAR     FileName[MAX_PATH]; 
    BOOLEAN  Reparse; 
    HANDLE   hFile; 
} IMAGEHLP_DEFERRED_SYMBOL_LOAD, *PIMAGEHLP_DEFERRED_SYMBOL_LOAD;
#endif
```

## -see-also

<a href="/windows/desktop/api/dbghelp/nc-dbghelp-psymbol_registered_callback">SymRegisterCallbackProc64</a>
