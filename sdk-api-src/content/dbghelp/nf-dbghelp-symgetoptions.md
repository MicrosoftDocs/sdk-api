---
UID: NF:dbghelp.SymGetOptions
title: SymGetOptions function (dbghelp.h)
description: Retrieves the current option mask.
helpviewer_keywords: ["SymGetOptions","SymGetOptions function","_win32_symgetoptions","base.symgetoptions","dbghelp/SymGetOptions"]
old-location: base\symgetoptions.htm
tech.root: Debug
ms.assetid: 3d9db826-1c4a-46d6-b007-c0dd5e6b17cc
ms.date: 12/05/2018
ms.keywords: SymGetOptions, SymGetOptions function, _win32_symgetoptions, base.symgetoptions, dbghelp/SymGetOptions
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
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - SymGetOptions
 - dbghelp/SymGetOptions
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
 - SymGetOptions
---

# SymGetOptions function


## -description

Retrieves the current option mask.



## -returns

The 
function returns the current options that have been set. Zero is a valid value and indicates that all options are turned off.

## -remarks

These options can be changed several times while the library is in use by an application. Any option change affects all future calls to the symbol handler.

The return value is the combination of the 
following values that have been set using the <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetoptions">SymSetOptions</a> function.

<ul>
<li>SYMOPT_ALLOW_ABSOLUTE_SYMBOLS</li>
<li>SYMOPT_ALLOW_ZERO_ADDRESS</li>
<li>SYMOPT_AUTO_PUBLICS</li>
<li>SYMOPT_CASE_INSENSITIVE</li>
<li>SYMOPT_DEBUG</li>
<li>SYMOPT_DEFERRED_LOADS</li>
<li>SYMOPT_EXACT_SYMBOLS</li>
<li>SYMOPT_FAIL_CRITICAL_ERRORS</li>
<li>SYMOPT_FAVOR_COMPRESSED</li>
<li>SYMOPT_FLAT_DIRECTORY</li>
<li>SYMOPT_IGNORE_CVREC</li>
<li>SYMOPT_IGNORE_IMAGEDIR</li>
<li>SYMOPT_IGNORE_NT_SYMPATH</li>
<li>SYMOPT_INCLUDE_32BIT_MODULES</li>
<li>SYMOPT_LOAD_ANYTHING</li>
<li>SYMOPT_LOAD_LINES</li>
<li>SYMOPT_NO_CPP</li>
<li>SYMOPT_NO_IMAGE_SEARCH</li>
<li>SYMOPT_NO_PROMPTS</li>
<li>SYMOPT_NO_PUBLICS</li>
<li>SYMOPT_NO_UNQUALIFIED_LOADS</li>
<li>SYMOPT_OVERWRITE</li>
<li>SYMOPT_PUBLICS_ONLY</li>
<li>SYMOPT_SECURE</li>
<li>SYMOPT_UNDNAME</li>
</ul>
All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>
