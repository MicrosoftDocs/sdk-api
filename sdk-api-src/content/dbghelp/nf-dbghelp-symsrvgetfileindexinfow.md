---
UID: NF:dbghelp.SymSrvGetFileIndexInfoW
title: SymSrvGetFileIndexInfoW function (dbghelp.h)
description: The SymSrvGetFileIndexInfoW (Unicode) function (dbghelp.h) retrieves the index information for the specified .pdb, .dbg, or image file.
helpviewer_keywords: ["SymSrvGetFileIndexInfo","SymSrvGetFileIndexInfo function","SymSrvGetFileIndexInfoW","base.symsrvgetfileindexinfo","dbghelp/SymSrvGetFileIndexInfo","dbghelp/SymSrvGetFileIndexInfoW"]
old-location: base\symsrvgetfileindexinfo.htm
tech.root: Debug
ms.assetid: ee5b0821-2746-467e-9d95-90776882ac95
ms.date: 08/04/2022
ms.keywords: SymSrvGetFileIndexInfo, SymSrvGetFileIndexInfo function, SymSrvGetFileIndexInfoW, base.symsrvgetfileindexinfo, dbghelp/SymSrvGetFileIndexInfo, dbghelp/SymSrvGetFileIndexInfoW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymSrvGetFileIndexInfoW (Unicode) and SymSrvGetFileIndexInfo (ANSI)
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
req.redist: DbgHelp.dll 6.6 or later
ms.custom: 19H1
f1_keywords:
 - SymSrvGetFileIndexInfoW
 - dbghelp/SymSrvGetFileIndexInfoW
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
 - SymSrvGetFileIndexInfo
 - SymSrvGetFileIndexInfo
 - SymSrvGetFileIndexInfoW
---

# SymSrvGetFileIndexInfoW function


## -description

Retrieves the index information for the specified .pdb, .dbg, or image file.

## -parameters

### -param File [in]

The name of the file.

### -param Info [out]

A <a href="/windows/desktop/api/dbghelp/ns-dbghelp-symsrv_index_info">SYMSRV_INDEX_INFO</a> structure that receives the index information.

### -param Flags [in]

This parameter is reserved for future use.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.
						

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function is not for general use.  Those writing utilities for the management of files in symbol server stores may use to this function to predict the relative path the symbol server will look for a file.  It is used by srctool.exe to actually populate symbol server stores.  It may also be of use to those looking to find the parameters to feed the <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symfindfileinpath">SymFindFileInPath</a> function.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.





> [!NOTE]
> The dbghelp.h header defines SymSrvGetFileIndexInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-symsrv_index_info">SYMSRV_INDEX_INFO</a>
