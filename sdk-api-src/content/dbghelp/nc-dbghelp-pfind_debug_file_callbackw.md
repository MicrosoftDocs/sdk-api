---
UID: NC:dbghelp.PFIND_DEBUG_FILE_CALLBACKW
title: PFIND_DEBUG_FILE_CALLBACKW (dbghelp.h)
description: An application-defined callback function used with the FindDebugInfoFileEx function. It verifies whether the symbol file located by FindDebugInfoFileEx is the correct symbol file.
helpviewer_keywords: ["FindDebugInfoFileProc","FindDebugInfoFileProc callback","FindDebugInfoFileProc callback function","PFIND_DEBUG_FILE_CALLBACK","PFIND_DEBUG_FILE_CALLBACKW","_win32_finddebuginfofileproc","base.finddebuginfofileproc","dbghelp/FindDebugInfoFileProc"]
old-location: base\finddebuginfofileproc.htm
tech.root: Debug
ms.assetid: c7ccc66a-7897-4430-8874-a4ba66a5cce7
ms.date: 12/05/2018
ms.keywords: FindDebugInfoFileProc, FindDebugInfoFileProc callback, FindDebugInfoFileProc callback function, PFIND_DEBUG_FILE_CALLBACK, PFIND_DEBUG_FILE_CALLBACKW, _win32_finddebuginfofileproc, base.finddebuginfofileproc, dbghelp/FindDebugInfoFileProc
f1_keywords:
- dbghelp/FindDebugInfoFileProc
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- DbgHelp.h
api_name:
- FindDebugInfoFileProc
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
---

# PFIND_DEBUG_FILE_CALLBACKW callback function


## -description


An application-defined callback function used with the 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-finddebuginfofileex">FindDebugInfoFileEx</a> function. It verifies whether the symbol file located by 
<b>FindDebugInfoFileEx</b> is the correct symbol file.

The <b>PFIND_DEBUG_FILE_CALLBACK</b> and <b>PFIND_DEBUG_FILE_CALLBACKW</b> types define a pointer to this callback function. 
<b>FindDebugInfoFileProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param FileHandle [in]

A handle to the symbol file.


### -param FileName [in]

The name of the symbol file.


### -param CallerData [in]

Optional user-defined data. This parameter can be <b>NULL</b>.


## -returns



If the symbol file is valid, return <b>TRUE</b>. Otherwise, return <b>FALSE</b>.




## -remarks



One way to verify the symbol file is to compare its timestamp to the timestamp in the image. To retrieve the timestamp of the image, use the 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-gettimestampforloadedlibrary">GetTimestampForLoadedLibrary</a> function. To retrieve the timestamp of the symbol file, use the 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symgetmoduleinfo">SymGetModuleInfo64</a> function.





> [!NOTE]
> The dbghelp.h header defines PFIND_DEBUG_FILE_CALLBACK as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-finddebuginfofileex">FindDebugInfoFileEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-gettimestampforloadedlibrary">GetTimestampForLoadedLibrary</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symgetmoduleinfo">SymGetModuleInfo64</a>
 

 

