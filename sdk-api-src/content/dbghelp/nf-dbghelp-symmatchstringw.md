---
UID: NF:dbghelp.SymMatchStringW
title: SymMatchStringW function
author: windows-sdk-content
description: Compares the specified string to the specified wildcard expression.
old-location: base\symmatchstring.htm
tech.root: debug
ms.assetid: 8423d14c-4ad7-453d-82d2-72e41492ac15
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: SymMatchString, SymMatchString function, SymMatchStringW, base.symmatchstring, dbghelp/SymMatchString, dbghelp/SymMatchStringW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.2 or later
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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>
 

 

