---
UID: NS:dbghelp._IMAGEHLP_LINEW64
title: IMAGEHLP_LINEW64 (dbghelp.h)
description: Represents a source file line. (IMAGEHLP_LINEW64)
helpviewer_keywords: ["*PIMAGEHLP_LINEW64","IMAGEHLP_LINE","IMAGEHLP_LINE structure","IMAGEHLP_LINE64","IMAGEHLP_LINE64 structure","IMAGEHLP_LINEW64","PIMAGEHLP_LINE64","PIMAGEHLP_LINE64 structure pointer","_IMAGEHLP_LINE64","_win32_imagehlp_line64_str","base.imagehlp_line64_str","dbghelp/IMAGEHLP_LINE64","dbghelp/IMAGEHLP_LINEW64","dbghelp/PIMAGEHLP_LINE64"]
old-location: base\imagehlp_line64_str.htm
tech.root: Debug
ms.assetid: 62124983-8381-4eb4-94f6-220b844aca45
ms.date: 12/05/2018
ms.keywords: '*PIMAGEHLP_LINEW64, IMAGEHLP_LINE, IMAGEHLP_LINE structure, IMAGEHLP_LINE64, IMAGEHLP_LINE64 structure, IMAGEHLP_LINEW64, PIMAGEHLP_LINE64, PIMAGEHLP_LINE64 structure pointer, _IMAGEHLP_LINE64, _win32_imagehlp_line64_str, base.imagehlp_line64_str, dbghelp/IMAGEHLP_LINE64, dbghelp/IMAGEHLP_LINEW64, dbghelp/PIMAGEHLP_LINE64'
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: IMAGEHLP_LINEW64 (Unicode) and IMAGEHLP_LINE64 (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IMAGEHLP_LINEW64, *PIMAGEHLP_LINEW64
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _IMAGEHLP_LINEW64
 - dbghelp/_IMAGEHLP_LINEW64
 - PIMAGEHLP_LINEW64
 - dbghelp/PIMAGEHLP_LINEW64
 - IMAGEHLP_LINEW64
 - dbghelp/IMAGEHLP_LINEW64
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
 - IMAGEHLP_LINE64
 - IMAGEHLP_LINE64
 - IMAGEHLP_LINEW64
 - IMAGEHLP_LINE
---

# IMAGEHLP_LINEW64 structure


## -description

Represents a source file line.

## -struct-fields

### -field SizeOfStruct

The size of the structure, in bytes. The caller must set this member to <code>sizeof(IMAGEHLP_LINE64)</code>.

### -field Key

This member is reserved for use by the operating system.

### -field LineNumber

The line number in the file.

### -field FileName

The name of the file, including the full path.

### -field Address

The address of the first instruction in the line.

## -remarks

This structure supersedes the <b>IMAGEHLP_LINE</b> structure. For more information, see 
<a href="/windows/desktop/Debug/updated-platform-support">Updated Platform Support</a>. <b>IMAGEHLP_LINE</b> is defined as follows in DbgHelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define IMAGEHLP_LINE IMAGEHLP_LINE64
#define PIMAGEHLP_LINE PIMAGEHLP_LINE64
#else
typedef struct _IMAGEHLP_LINE {
    DWORD    SizeOfStruct; 
    PVOID    Key; 
    DWORD    LineNumber; 
    PCHAR    FileName; 
    DWORD    Address; 
} IMAGEHLP_LINE, *PIMAGEHLP_LINE;

typedef struct _IMAGEHLP_LINEW {
    DWORD    SizeOfStruct; 
    PVOID    Key; 
    DWORD    LineNumber; 
    PCHAR    FileName; 
    DWORD64  Address; 
} IMAGEHLP_LINEW, *PIMAGEHLP_LINEW;
#endif
```

## -see-also

<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetlinefromaddr">SymGetLineFromAddr64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetlinefromname">SymGetLineFromName64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetlinenext">SymGetLineNext64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetlineprev">SymGetLinePrev64</a>
