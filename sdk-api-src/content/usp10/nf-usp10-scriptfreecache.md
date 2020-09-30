---
UID: NF:usp10.ScriptFreeCache
title: ScriptFreeCache function (usp10.h)
description: Frees a script cache.
helpviewer_keywords: ["ScriptFreeCache","ScriptFreeCache function [Internationalization for Windows Applications]","_win32_ScriptFreeCache","intl.scriptfreecache","usp10/ScriptFreeCache"]
old-location: intl\scriptfreecache.htm
tech.root: Intl
ms.assetid: a30a6c5a-157a-47ad-b946-502d583733c8
ms.date: 12/05/2018
ms.keywords: ScriptFreeCache, ScriptFreeCache function [Internationalization for Windows Applications], _win32_ScriptFreeCache, intl.scriptfreecache, usp10/ScriptFreeCache
req.header: usp10.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Usp10.lib
req.dll: Usp10.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 5 or later on Windows Me/98/95
ms.custom: 19H1
f1_keywords:
 - ScriptFreeCache
 - usp10/ScriptFreeCache
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - usp10.dll
 - Ext-MS-Win-usp10-l1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptFreeCache
---

# ScriptFreeCache function


## -description

Frees a script cache.

## -parameters

### -param psc [in, out]

Pointer to the <a href="/windows/desktop/Intl/script-cache">SCRIPT_CACHE</a> structure.

## -returns

Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. The application cant test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.

## -remarks

An application can free the script cache at any time, with certain limitations if the application is multi-threaded. Uniscribe maintains reference counts in its <a href="/windows/desktop/Intl/caching">font and shaper caches</a> and frees font data only when all sizes of the font are free. It frees shaper data only when all supported fonts are freed.

The application should free the script cache for a style when it discards that style.

<b>ScriptFreeCache</b> always sets its parameter to <b>NULL</b> to help avoid misreferencing.

Uniscribe functions are re-entrant. Cache creation is interlocked through a single process-wide semaphore. <b>ScriptFreeCache</b> should not be called at a time when another thread might be accessing the particular cache to free. For performance reasons, the cache is not locked during <a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a> or <a href="/windows/desktop/api/usp10/nf-usp10-scriptplace">ScriptPlace</a>.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Intl/caching">Caching</a>



<a href="/windows/desktop/Intl/script-cache">SCRIPT_CACHE</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>