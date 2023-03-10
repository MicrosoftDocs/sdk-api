---
UID: NS:dbghelp._IMAGEHLP_MODULE
title: IMAGEHLP_MODULE (dbghelp.h)
description: Contains module information. (IMAGEHLP_MODULE)
helpviewer_keywords: ["*PIMAGEHLP_MODULE","IMAGEHLP_MODULE","IMAGEHLP_MODULE structure","IMAGEHLP_MODULE64","IMAGEHLP_MODULE64 structure","IMAGEHLP_MODULEW64","PIMAGEHLP_MODULE64","PIMAGEHLP_MODULE64 structure pointer","SymCoff","SymCv","SymDeferred","SymDia","SymExport","SymNone","SymPdb","SymSym","SymVirtual","_IMAGEHLP_MODULE64","_win32_imagehlp_module64_str","base.imagehlp_module64_str","dbghelp/IMAGEHLP_MODULE64","dbghelp/IMAGEHLP_MODULEW64","dbghelp/PIMAGEHLP_MODULE64"]
old-location: base\imagehlp_module64_str.htm
tech.root: Debug
ms.assetid: 3cc7a678-561b-4af8-8cf0-5cf6ebc0cb26
ms.date: 12/05/2018
ms.keywords: '*PIMAGEHLP_MODULE, IMAGEHLP_MODULE, IMAGEHLP_MODULE structure, IMAGEHLP_MODULE64, IMAGEHLP_MODULE64 structure, IMAGEHLP_MODULEW64, PIMAGEHLP_MODULE64, PIMAGEHLP_MODULE64 structure pointer, SymCoff, SymCv, SymDeferred, SymDia, SymExport, SymNone, SymPdb, SymSym, SymVirtual, _IMAGEHLP_MODULE64, _win32_imagehlp_module64_str, base.imagehlp_module64_str, dbghelp/IMAGEHLP_MODULE64, dbghelp/IMAGEHLP_MODULEW64, dbghelp/PIMAGEHLP_MODULE64'
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: IMAGEHLP_MODULEW64 (Unicode) and IMAGEHLP_MODULE64 (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IMAGEHLP_MODULE, *PIMAGEHLP_MODULE
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _IMAGEHLP_MODULE
 - dbghelp/_IMAGEHLP_MODULE
 - PIMAGEHLP_MODULE
 - dbghelp/PIMAGEHLP_MODULE
 - IMAGEHLP_MODULE
 - dbghelp/IMAGEHLP_MODULE
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
 - IMAGEHLP_MODULE64
 - IMAGEHLP_MODULE64
 - IMAGEHLP_MODULEW64
 - IMAGEHLP_MODULE
---

## -description

Contains module information.

## -struct-fields

### -field SizeOfStruct

The size of the structure, in bytes. The caller must set this member to <code>sizeof(IMAGEHLP_MODULE64)</code>.

### -field BaseOfImage

The base virtual address where the image is loaded.

### -field ImageSize

The size of the image, in bytes.

### -field TimeDateStamp

The date and timestamp value. The value is represented in the number of seconds elapsed since midnight (00:00:00), January 1, 1970, Universal Coordinated Time, according to the system clock. The timestamp can be printed using the C run-time (CRT) function <b>ctime</b>.

### -field CheckSum

The checksum of the image. This value can be zero.

### -field NumSyms

The number of symbols in the symbol table.  The value of this parameter is not meaningful when <b>SymPdb</b> is specified as  the value of the <i>SymType</i> parameter.

### -field SymType

The type of symbols that are loaded. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SymCoff"></a><a id="symcoff"></a><a id="SYMCOFF"></a><dl>
<dt><b>SymCoff</b></dt>
</dl>
</td>
<td width="60%">
COFF symbols.

</td>
</tr>
<tr>
<td width="40%"><a id="SymCv"></a><a id="symcv"></a><a id="SYMCV"></a><dl>
<dt><b>SymCv</b></dt>
</dl>
</td>
<td width="60%">
CodeView symbols.

</td>
</tr>
<tr>
<td width="40%"><a id="SymDeferred"></a><a id="symdeferred"></a><a id="SYMDEFERRED"></a><dl>
<dt><b>SymDeferred</b></dt>
</dl>
</td>
<td width="60%">
Symbol loading deferred.

</td>
</tr>
<tr>
<td width="40%"><a id="SymDia"></a><a id="symdia"></a><a id="SYMDIA"></a><dl>
<dt><b>SymDia</b></dt>
</dl>
</td>
<td width="60%">
DIA symbols.

</td>
</tr>
<tr>
<td width="40%"><a id="SymExport"></a><a id="symexport"></a><a id="SYMEXPORT"></a><dl>
<dt><b>SymExport</b></dt>
</dl>
</td>
<td width="60%">
Symbols generated from a DLL export table.

</td>
</tr>
<tr>
<td width="40%"><a id="SymNone"></a><a id="symnone"></a><a id="SYMNONE"></a><dl>
<dt><b>SymNone</b></dt>
</dl>
</td>
<td width="60%">
No symbols are loaded.

</td>
</tr>
<tr>
<td width="40%"><a id="SymPdb"></a><a id="sympdb"></a><a id="SYMPDB"></a><dl>
<dt><b>SymPdb</b></dt>
</dl>
</td>
<td width="60%">
PDB symbols.

</td>
</tr>
<tr>
<td width="40%"><a id="SymSym"></a><a id="symsym"></a><a id="SYMSYM"></a><dl>
<dt><b>SymSym</b></dt>
</dl>
</td>
<td width="60%">
.sym file.

</td>
</tr>
<tr>
<td width="40%"><a id="SymVirtual"></a><a id="symvirtual"></a><a id="SYMVIRTUAL"></a><dl>
<dt><b>SymVirtual</b></dt>
</dl>
</td>
<td width="60%">
The virtual module created by 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symloadmoduleex">SymLoadModuleEx</a> with <b>SLMFLAG_VIRTUAL</b>.
							

</td>
</tr>
</table>

### -field ModuleName

The module name.

### -field ImageName

The image name. The name may or may not contain a full path.

### -field LoadedImageName

The full path and file name of the file from which symbols were loaded.

## -remarks

This structure supersedes the <b>IMAGEHLP_MODULE</b> structure. For more information, see 
<a href="/windows/desktop/Debug/updated-platform-support">Updated Platform Support</a>. <b>IMAGEHLP_MODULE</b> is defined as follows in DbgHelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define IMAGEHLP_MODULE IMAGEHLP_MODULE64
#define PIMAGEHLP_MODULE PIMAGEHLP_MODULE64
#define IMAGEHLP_MODULEW IMAGEHLP_MODULEW64
#define PIMAGEHLP_MODULEW PIMAGEHLP_MODULEW64
#else
typedef struct _IMAGEHLP_MODULE {
    DWORD    SizeOfStruct;
    DWORD    BaseOfImage; 
    DWORD    ImageSize; 
    DWORD    TimeDateStamp; 
    DWORD    CheckSum; 
    DWORD    NumSyms; 
    SYM_TYPE SymType; 
    CHAR     ModuleName[32];  
    CHAR     ImageName[256]; 
    CHAR     LoadedImageName[256]; 
} IMAGEHLP_MODULE, *PIMAGEHLP_MODULE;

typedef struct _IMAGEHLP_MODULEW {
    DWORD    SizeOfStruct;  
    DWORD    BaseOfImage; 
    DWORD    ImageSize;  
    DWORD    TimeDateStamp; 
    DWORD    CheckSum; 
    DWORD    NumSyms; 
    SYM_TYPE SymType; 
    WCHAR    ModuleName[32]; 
    WCHAR    ImageName[256]; 
    WCHAR    LoadedImageName[256]; 
} IMAGEHLP_MODULEW, *PIMAGEHLP_MODULEW;
#endif
```

## -see-also

<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetmoduleinfo">SymGetModuleInfo64</a>
