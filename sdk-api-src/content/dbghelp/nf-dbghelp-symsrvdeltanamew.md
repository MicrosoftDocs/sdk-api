---
UID: NF:dbghelp.SymSrvDeltaNameW
title: SymSrvDeltaNameW function (dbghelp.h)
description: The SymSrvDeltaNameW (Unicode) function (dbghelp.h) generates the name for a file that describes the relationship between two versions of the same symbol/image.
helpviewer_keywords: ["SymSrvDeltaName","SymSrvDeltaName function","SymSrvDeltaNameW","base.symsrvdeltaname","dbghelp/SymSrvDeltaName","dbghelp/SymSrvDeltaNameW"]
old-location: base\symsrvdeltaname.htm
tech.root: Debug
ms.assetid: 35be6aff-efc7-4ed9-bfe7-3d0f798acbd9
ms.date: 08/04/2022
ms.keywords: SymSrvDeltaName, SymSrvDeltaName function, SymSrvDeltaNameW, base.symsrvdeltaname, dbghelp/SymSrvDeltaName, dbghelp/SymSrvDeltaNameW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymSrvDeltaNameW (Unicode) and SymSrvDeltaName (ANSI)
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
req.redist: DbgHelp.dll 6.3 or later
ms.custom: 19H1
f1_keywords:
 - SymSrvDeltaNameW
 - dbghelp/SymSrvDeltaNameW
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
 - SymSrvDeltaName
 - SymSrvDeltaName
 - SymSrvDeltaNameW
---

# SymSrvDeltaNameW function


## -description

Generates the name for a file that describes the relationship between two different versions of the same symbol or image file.
		Using this feature prevents applications from having to regenerate such information every time they analyze two files.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param SymPath [in, optional]

The symbol path. The function uses only the symbol stores described in standard syntax for symbol stores. All other paths are ignored. If this parameter is <b>NULL</b>, the function uses the symbol path set using the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> or <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetsearchpath">SymSetSearchPath</a> function.

### -param Type [in]

The extension for the generated file name.

### -param File1 [in]

The path of the first version of the symbol or image file.

### -param File2 [in]

The path of the second version of the symbol or image file.

## -returns

If the function succeeds, the return value is the resulting file name.
						

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function opens the two specified files, reads the indexing information from the header, and passes this information to the symbol server so it can create the file name. If you specify the <i>Type</i> parameter as "xml", the name is the index of <i>File1</i>, followed by a dash, followed by the index of <i>File2</i>, followed by an .xml extension. For example:

3F3D5C755000-3F3D647621000.xml

This function returns a pointer to a buffer that may be reused by another function. Therefore, be sure to copy the data returned to another buffer immediately.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.





> [!NOTE]
> The dbghelp.h header defines SymSrvDeltaName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>
