---
UID: NS:dbghelp._IMAGEHLP_SYMBOLW64
title: IMAGEHLP_SYMBOLW64 (dbghelp.h)
description: Contains symbol information. (IMAGEHLP_SYMBOLW64)
helpviewer_keywords: ["*PIMAGEHLP_SYMBOLW64","IMAGEHLP_SYMBOL","IMAGEHLP_SYMBOL structure","IMAGEHLP_SYMBOL64","IMAGEHLP_SYMBOL64 structure","IMAGEHLP_SYMBOLW64","PIMAGEHLP_SYMBOL64","PIMAGEHLP_SYMBOL64 structure pointer","_IMAGEHLP_SYMBOL64","_win32_imagehlp_symbol64_str","base.imagehlp_symbol64_str","dbghelp/IMAGEHLP_SYMBOL64","dbghelp/IMAGEHLP_SYMBOLW64","dbghelp/PIMAGEHLP_SYMBOL64"]
old-location: base\imagehlp_symbol64_str.htm
tech.root: Debug
ms.assetid: 7b39281a-c34b-47ae-a3ff-5f0a7a66a588
ms.date: 12/05/2018
ms.keywords: '*PIMAGEHLP_SYMBOLW64, IMAGEHLP_SYMBOL, IMAGEHLP_SYMBOL structure, IMAGEHLP_SYMBOL64, IMAGEHLP_SYMBOL64 structure, IMAGEHLP_SYMBOLW64, PIMAGEHLP_SYMBOL64, PIMAGEHLP_SYMBOL64 structure pointer, _IMAGEHLP_SYMBOL64, _win32_imagehlp_symbol64_str, base.imagehlp_symbol64_str, dbghelp/IMAGEHLP_SYMBOL64, dbghelp/IMAGEHLP_SYMBOLW64, dbghelp/PIMAGEHLP_SYMBOL64'
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: IMAGEHLP_SYMBOLW64 (Unicode) and IMAGEHLP_SYMBOL64 (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IMAGEHLP_SYMBOLW64, *PIMAGEHLP_SYMBOLW64
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _IMAGEHLP_SYMBOLW64
 - dbghelp/_IMAGEHLP_SYMBOLW64
 - PIMAGEHLP_SYMBOLW64
 - dbghelp/PIMAGEHLP_SYMBOLW64
 - IMAGEHLP_SYMBOLW64
 - dbghelp/IMAGEHLP_SYMBOLW64
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
 - IMAGEHLP_SYMBOL64
 - IMAGEHLP_SYMBOL64
 - IMAGEHLP_SYMBOLW64
 - IMAGEHLP_SYMBOL
---

# IMAGEHLP_SYMBOLW64 structure


## -description

Contains symbol information.

## -struct-fields

### -field SizeOfStruct

The size of the structure, in bytes. The caller must set this member to <code>sizeof(IMAGEHLP_SYMBOL64)</code>.

### -field Address

The virtual address for the symbol.

### -field Size

The size of the symbol, in bytes. This value is a best guess and can be zero.

### -field Flags

This member is reserved for use by the operating system.

### -field MaxNameLength

The maximum length of the string that the <b>Name</b> member can contain, in characters, not including the null-terminating character. Because symbol names can vary in length, this data structure is allocated by the caller. This member is used so the library knows how much memory is available for use by the symbol name.

### -field Name

The decorated or undecorated symbol name. If the buffer is not large enough for the complete name, it is truncated to <b>MaxNameLength</b> characters, including the null-terminating character.

## -remarks

This structure supersedes the <b>IMAGEHLP_SYMBOL</b> structure. For more information, see 
<a href="/windows/desktop/Debug/updated-platform-support">Updated Platform Support</a>. <b>IMAGEHLP_SYMBOL</b> is defined as follows in DbgHelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
 #define IMAGEHLP_SYMBOL IMAGEHLP_SYMBOL64
 #define PIMAGEHLP_SYMBOL PIMAGEHLP_SYMBOL64
#else
 typedef struct _IMAGEHLP_SYMBOL {
     DWORD SizeOfStruct; 
     DWORD Address; 
     DWORD Size; 
     DWORD Flags;  
     DWORD MaxNameLength; 
     CHAR  Name[1];  
 } IMAGEHLP_SYMBOL, *PIMAGEHLP_SYMBOL;
#endif
```

## -see-also

<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetsymfromaddr">SymGetSymFromAddr64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetsymfromname">SymGetSymFromName64</a>
