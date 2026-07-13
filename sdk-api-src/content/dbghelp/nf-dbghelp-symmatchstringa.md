---
UID: NF:dbghelp.SymMatchStringA
tech.root: Debug 
title: SymMatchStringA
ms.date: 04/14/2021
targetos: Windows
description: Compares the specified string to the specified wildcard expression. (SymMatchStringA)
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Dbghelp.dll 
req.header: dbghelp.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Dbghelp.lib 
req.max-support: 
req.namespace: 
req.redist: DbgHelp.dll 6.2 or later 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: Windows 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
api_name:
 - SymMatchStringA
 - SymMatchString
f1_keywords:
 - SymMatchStringA
 - dbghelp/SymMatchStringA
 - SymMatchString
 - dbghelp/SymMatchString
dev_langs:
 - c++
---

# SymMatchStringA function

## -description

Compares the specified string to the specified wildcard expression.

## -parameters

### -param string [in]

The string, such as a symbol name, to be compared to the <i>expression</i> parameter.

### -param expression [in]

The wildcard expression to compare to the <i>string</i> parameter. The wildcard expression supports the inclusion of the * and ? characters. * matches any string and ? matches any single character.

### -param fCase [in]

A variable that indicates whether or not the comparison is to be case sensitive.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.  

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

> [!NOTE]
> The dbghelp.h header defines SymMatchString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>  
