---
UID: NC:dbghelp.PENUMDIRTREE_CALLBACKW
title: PENUMDIRTREE_CALLBACKW (dbghelp.h)
description: PENUMDIRTREE_CALLBACKW (Unicode) is an application-defined callback function used with the EnumDirTree function. It is called every time a match is found.
helpviewer_keywords: ["EnumDirTreeProc","EnumDirTreeProc callback","EnumDirTreeProc callback function","PENUMDIRTREE_CALLBACK","PENUMDIRTREE_CALLBACKW","_win32_enumdirtreeproc","base.enumdirtreeproc","dbghelp/EnumDirTreeProc"]
old-location: base\enumdirtreeproc.htm
tech.root: Debug
ms.assetid: eae41b83-bba5-4656-9a5c-b6ef56845954
ms.date: 08/03/2022
ms.keywords: EnumDirTreeProc, EnumDirTreeProc callback, EnumDirTreeProc callback function, PENUMDIRTREE_CALLBACK, PENUMDIRTREE_CALLBACKW, _win32_enumdirtreeproc, base.enumdirtreeproc, dbghelp/EnumDirTreeProc
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
req.redist: DbgHelp.dll 6.0 or later
ms.custom: 19H1
f1_keywords:
 - PENUMDIRTREE_CALLBACKW
 - dbghelp/PENUMDIRTREE_CALLBACKW
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
 - EnumDirTreeProc
---

# PENUMDIRTREE_CALLBACKW callback function


## -description

An application-defined callback function used with the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-enumdirtree">EnumDirTree</a> function. It is called every time a match is found.

The <b>PENUMDIRTREE_CALLBACK</b> and <b>PENUMDIRTREE_CALLBACKW</b> types define a pointer to this callback function. 
<i>EnumDirTreeProc</i> is a placeholder for the application-defined function name.

## -parameters

### -param FilePath [in]

A pointer to a buffer that receives the full path of the file that is found.

### -param CallerData [in, optional]

A user-defined value specified in 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-enumdirtree">EnumDirTree</a>, or <b>NULL</b>. Typically, this parameter is used by an application to pass a pointer to a data structure that enables the callback function to establish some context.

## -returns

To continue enumeration, the callback function must return <b>FALSE</b>.

To stop enumeration, the callback function must return <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-enumdirtree">EnumDirTree</a>

## -remarks

> [!NOTE]
> The dbghelp.h header defines PENUMDIRTREE_CALLBACK as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
