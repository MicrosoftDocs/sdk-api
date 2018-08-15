---
UID: NF:usp10.ScriptFreeCache
title: ScriptFreeCache function
author: windows-sdk-content
description: Frees a script cache.
old-location: intl\scriptfreecache.htm
old-project: Intl
ms.assetid: a30a6c5a-157a-47ad-b946-502d583733c8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ScriptFreeCache, ScriptFreeCache function [Internationalization for Windows Applications], _win32_ScriptFreeCache, intl.scriptfreecache, usp10/ScriptFreeCache
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: usp10.h
req.include-header: 
req.redist: Internet Explorer 5 or later on Windows Me/98/95
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
tech.root: 
req.typenames: SCRIPT_JUSTIFY
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
product: Windows
targetos: Windows
req.lib: Usp10.lib
req.dll: Usp10.dll
req.irql: 
req.product: Windows UI
---

# ScriptFreeCache function


## -description


Frees a script cache.


## -parameters




### -param psc [in, out]

Pointer to the <a href="https://msdn.microsoft.com/56a98529-6ae9-4b71-bd7d-cf056a1e3683">SCRIPT_CACHE</a> structure.


## -returns



Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. The application cant test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.




## -remarks



An application can free the script cache at any time, with certain limitations if the application is multi-threaded. Uniscribe maintains reference counts in its <a href="https://msdn.microsoft.com/c06c0eaf-41cb-4fd1-9750-a78355217f12">font and shaper caches</a> and frees font data only when all sizes of the font are free. It frees shaper data only when all supported fonts are freed.

The application should free the script cache for a style when it discards that style.

<b>ScriptFreeCache</b> always sets its parameter to <b>NULL</b> to help avoid misreferencing.

Uniscribe functions are re-entrant. Cache creation is interlocked through a single process-wide semaphore. <b>ScriptFreeCache</b> should not be called at a time when another thread might be accessing the particular cache to free. For performance reasons, the cache is not locked during <a href="https://msdn.microsoft.com/073ba94a-ebfa-42f5-9d90-d5693dc25703">ScriptShape</a> or <a href="https://msdn.microsoft.com/7f88432f-052f-4781-8346-31c8a0771e51">ScriptPlace</a>.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c06c0eaf-41cb-4fd1-9750-a78355217f12">Caching</a>



<a href="https://msdn.microsoft.com/56a98529-6ae9-4b71-bd7d-cf056a1e3683">SCRIPT_CACHE</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/876e36f5-a91c-490b-87bd-b7cb4993f8c4">Uniscribe Functions</a>
 

 

