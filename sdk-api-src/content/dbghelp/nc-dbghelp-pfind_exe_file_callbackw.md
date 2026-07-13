---
UID: NC:dbghelp.PFIND_EXE_FILE_CALLBACKW
title: PFIND_EXE_FILE_CALLBACKW (dbghelp.h)
description: PFIND_EXE_FILE_CALLBACKW (Unicode) is an application-defined callback function used with the FindExecutableImageEx function. It verifies whether the executable file found by FindExecutableImageEx is the correct executable file.
helpviewer_keywords: ["FindExecutableImageProc","FindExecutableImageProc callback","FindExecutableImageProc callback function","PFIND_EXE_FILE_CALLBACK","PFIND_EXE_FILE_CALLBACKW","_win32_findexecutableimageproc","base.findexecutableimageproc","dbghelp/FindExecutableImageProc"]
old-location: base\findexecutableimageproc.htm
tech.root: Debug
ms.assetid: cbd8cd63-8fdb-4314-8737-9f934de74f89
ms.date: 08/03/2022
ms.keywords: FindExecutableImageProc, FindExecutableImageProc callback, FindExecutableImageProc callback function, PFIND_EXE_FILE_CALLBACK, PFIND_EXE_FILE_CALLBACKW, _win32_findexecutableimageproc, base.findexecutableimageproc, dbghelp/FindExecutableImageProc
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
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - PFIND_EXE_FILE_CALLBACKW
 - dbghelp/PFIND_EXE_FILE_CALLBACKW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - DbgHelp.h
api_name:
 - FindExecutableImageProc
---

# PFIND_EXE_FILE_CALLBACKW callback function


## -description

An application-defined callback function used with the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-findexecutableimageex">FindExecutableImageEx</a> function. It verifies whether the executable file found by 
<b>FindExecutableImageEx</b> is the correct executable file.

The <b>PFIND_EXE_FILE_CALLBACK</b> and <b>PFIND_EXE_FILE_CALLBACKW</b> types define a pointer to this callback function. 
<b>FindExecutableImageProc</b> is a placeholder for the application-defined function name.

## -parameters

### -param FileHandle [in]

A handle to the executable file.

### -param FileName [in]

The name of the executable file.

### -param CallerData [in]

Optional user-defined data. This parameter can be <b>NULL</b>.

## -returns

If the executable file is valid, return <b>TRUE</b>. Otherwise, return <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-findexecutableimageex">FindExecutableImageEx</a>

## -remarks

> [!NOTE]
> The dbghelp.h header defines PFIND_EXE_FILE_CALLBACK as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
