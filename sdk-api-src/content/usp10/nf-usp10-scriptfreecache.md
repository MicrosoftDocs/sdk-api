---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

