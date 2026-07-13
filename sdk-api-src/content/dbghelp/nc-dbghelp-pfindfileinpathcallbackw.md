---
UID: NC:dbghelp.PFINDFILEINPATHCALLBACKW
title: PFINDFILEINPATHCALLBACKW (dbghelp.h)
description: PFINDFILEINPATHCALLBACKW (Unicode) is an application-defined callback function used with the SymFindFileInPath function.
helpviewer_keywords: ["PFINDFILEINPATHCALLBACK","PFINDFILEINPATHCALLBACKW","SymFindFileInPathProc","SymFindFileInPathProc callback","SymFindFileInPathProc callback function","_win32_symfindfileinpathproc","base.symfindfileinpathproc","dbghelp/SymFindFileInPathProc"]
old-location: base\symfindfileinpathproc.htm
tech.root: Debug
ms.assetid: e579158e-053d-4c81-a2c3-ac3af3d3a201
ms.date: 08/03/2022
ms.keywords: PFINDFILEINPATHCALLBACK, PFINDFILEINPATHCALLBACKW, SymFindFileInPathProc, SymFindFileInPathProc callback, SymFindFileInPathProc callback function, _win32_symfindfileinpathproc, base.symfindfileinpathproc, dbghelp/SymFindFileInPathProc
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
 - PFINDFILEINPATHCALLBACKW
 - dbghelp/PFINDFILEINPATHCALLBACKW
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
 - SymFindFileInPathProc
---

## -description

An application-defined callback function used with the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symfindfileinpath">SymFindFileInPath</a> function.

The <b>PFINDFILEINPATHCALLBACK</b> and <b>PFINDFILEINPATHCALLBACKW</b> types define a pointer to this callback function. 
<b>SymFindFileInPathProc</b> is a placeholder for the application-defined function name.

## -parameters

### -param fileName [in]

The name of the file located by <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symfindfileinpath">SymFindFileInPath</a>.

### -param context [in]

The user-defined value specified in 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symfindfileinpath">SymFindFileInPath</a>, or <b>NULL</b>. This parameter is typically used by an application to pass a pointer to a data structure that provides some context for the callback function.

## -returns

Return <b>TRUE</b> to continue searching.

Return <b>FALSE</b> to end the search.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symfindfileinpath">SymFindFileInPath</a>

## -remarks

> [!NOTE]
> The dbghelp.h header defines PFINDFILEINPATHCALLBACK as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
