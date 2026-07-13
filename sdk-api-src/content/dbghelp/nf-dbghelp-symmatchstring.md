---
UID: NF:dbghelp.SymMatchString
title: SymMatchString function (dbghelp.h)
description: The SymMatchString function (dbghelp.h) compares the specified string to the specified wildcard expression.
helpviewer_keywords: ["SymMatchString","SymMatchString function","SymMatchStringW","base.symmatchstring","dbghelp/SymMatchString","dbghelp/SymMatchStringW"]
old-location: base\symmatchstring.htm
tech.root: Debug
ms.assetid: 8423d14c-4ad7-453d-82d2-72e41492ac15
ms.date: 08/04/2022
ms.keywords: SymMatchString, SymMatchString function, SymMatchStringW, base.symmatchstring, dbghelp/SymMatchString, dbghelp/SymMatchStringW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymMatchStringW (Unicode) and SymMatchString (ANSI)
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
req.redist: DbgHelp.dll 6.2 or later
ms.custom: 19H1
f1_keywords:
 - SymMatchString
 - dbghelp/SymMatchString
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
 - SymMatchString
 - SymMatchString
 - SymMatchStringW
---

# SymMatchString function


## -description

Compares the specified string to the specified wildcard expression.

## -parameters

### -param string [in]

The string, such as a symbol name, to be compared to the <i>expression</i> parameter.

### -param expression [in]

The wildcard expression to compare to the <i>string</i> parameter.  The wildcard expression supports the inclusion of the * and ? characters.  * matches any string and ? matches any single character.

### -param fCase [in]

A variable that indicates whether or not the comparison is to be case sensitive.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.
						

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>
