---
UID: NF:usp10.ScriptCacheGetHeight
title: ScriptCacheGetHeight function (usp10.h)
description: Retrieves the height of the currently cached font.
helpviewer_keywords: ["ScriptCacheGetHeight","ScriptCacheGetHeight function [Internationalization for Windows Applications]","_win32_ScriptCacheGetHeight","intl.scriptcachegetheight","usp10/ScriptCacheGetHeight"]
old-location: intl\scriptcachegetheight.htm
tech.root: Intl
ms.assetid: e147b0c4-7d9f-4961-8bce-25dab716f7a2
ms.date: 12/05/2018
ms.keywords: ScriptCacheGetHeight, ScriptCacheGetHeight function [Internationalization for Windows Applications], _win32_ScriptCacheGetHeight, intl.scriptcachegetheight, usp10/ScriptCacheGetHeight
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
 - ScriptCacheGetHeight
 - usp10/ScriptCacheGetHeight
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - usp10.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptCacheGetHeight
---

# ScriptCacheGetHeight function


## -description

Retrieves the height of the currently cached font.

## -parameters

### -param hdc [in]

Optional. Handle to the device context. For more information, see <a href="/windows/desktop/Intl/caching">Caching</a>.

### -param psc [in, out]

Pointer to a <a href="/windows/desktop/Intl/script-cache">SCRIPT_CACHE</a> structure identifying the script cache.

### -param tmHeight [out]

Pointer to a buffer in which the function retrieves the font height.

## -returns

Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.

## -remarks

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Intl/caching">Caching</a>



<a href="/windows/desktop/Intl/script-cache">SCRIPT_CACHE</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>