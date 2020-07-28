---
UID: NF:dbghelp.SymMatchStringW
title: SymMatchStringW function (dbghelp.h)
description: Compares the specified string to the specified wildcard expression.
helpviewer_keywords: ["SymMatchString","SymMatchString function","SymMatchStringW","base.symmatchstring","dbghelp/SymMatchString","dbghelp/SymMatchStringW"]
old-location: base\symmatchstring.htm
tech.root: Debug
ms.assetid: 8423d14c-4ad7-453d-82d2-72e41492ac15
ms.date: 12/05/2018
ms.keywords: SymMatchString, SymMatchString function, SymMatchStringW, base.symmatchstring, dbghelp/SymMatchString, dbghelp/SymMatchStringW
f1_keywords:
- dbghelp/SymMatchString
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
req.unicode-ansi: SymMatchStringW (Unicode) and SymMatchString (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.2 or later
ms.custom: 19H1
---

# SymMatchStringW function


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
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.





> [!NOTE]
> The dbghelp.h header defines SymMatchString as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>
 

 

