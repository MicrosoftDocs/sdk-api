---
UID: NF:dbghelp.SymMatchFileNameW
title: SymMatchFileNameW function (dbghelp.h)
description: The SymMatchFileNameW (Unicode) function compares a string to a file name and path.
helpviewer_keywords: ["SymMatchFileName","SymMatchFileName function","SymMatchFileNameW","_win32_symmatchfilename","base.symmatchfilename","dbghelp/SymMatchFileName","dbghelp/SymMatchFileNameW"]
old-location: base\symmatchfilename.htm
tech.root: Debug
ms.assetid: 69787cc7-db84-4c60-8d7d-f8eae18c82e9
ms.date: 08/04/2022
ms.keywords: SymMatchFileName, SymMatchFileName function, SymMatchFileNameW, _win32_symmatchfilename, base.symmatchfilename, dbghelp/SymMatchFileName, dbghelp/SymMatchFileNameW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymMatchFileNameW (Unicode) and SymMatchFileName (ANSI)
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
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - SymMatchFileNameW
 - dbghelp/SymMatchFileNameW
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
 - SymMatchFileName
 - SymMatchFileName
 - SymMatchFileNameW
---

# SymMatchFileNameW function


## -description

Compares a string to a file name and path.

## -parameters

### -param FileName [in]

The file name to be compared to the <i>Match</i> parameter.

### -param Match [in]

The string to be compared to the <i>FileName</i> parameter.

### -param FileNameStop [out, optional]

A pointer to a string buffer that receives a pointer to the location in <i>FileName</i> where matching stopped. For a complete match, this value can be one character before <i>FileName</i>. This value can also be <b>NULL</b>.

### -param MatchStop [out, optional]

A pointer to a string buffer that receives a pointer to the location in <i>Match</i> where matching stopped. For a complete match, this value may be one character before <i>Match</i>. This value may be <b>NULL</b>.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Because the match string can be a suffix of the complete file name, this function can be used to match a plain file name to a fully qualified file name.

Matching begins from the end of both strings and proceeds backward. Matching is case-insensitive and equates a backslash (\\) with a forward slash (/).

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.





> [!NOTE]
> The dbghelp.h header defines SymMatchFileName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>
