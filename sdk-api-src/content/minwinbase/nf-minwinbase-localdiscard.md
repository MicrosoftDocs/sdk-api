---
UID: NF:minwinbase.LocalDiscard
title: LocalDiscard macro (minwinbase.h)
description: Discards the specified local memory object. The lock count of the memory object must be zero.
helpviewer_keywords: ["LocalDiscard","LocalDiscard macro","_win32_localdiscard","base.localdiscard","minwinbase/LocalDiscard"]
old-location: base\localdiscard.htm
tech.root: base
ms.assetid: 05842fa7-0438-4237-962f-055dc338368c
ms.date: 07/01/2025
ms.keywords: LocalDiscard, LocalDiscard macro, _win32_localdiscard, base.localdiscard, minwinbase/LocalDiscard
req.header: minwinbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LocalDiscard
 - minwinbase/LocalDiscard
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minwinbase.h
api_name:
 - LocalDiscard
---

# LocalDiscard macro

## -syntax

```cpp
HLOCAL LocalDiscard(
  [in]  HLOCAL h
);
```

## -returns

Type: **[HLOCAL](/windows/desktop/winprog/windows-data-types)**

If the function succeeds, the return value is a handle to the local memory object.If the function fails, the return value is **NULL**. To get extended error information, call [GetLastError](/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).


## -description

Discards the specified local memory object. The lock count of the memory object must be zero.
<div class="alert"><b>Note</b>  The local functions have greater overhead and provide fewer features than other memory management functions. New applications should use the <a href="/windows/desktop/Memory/heap-functions">heap functions</a> unless documentation states that a local function should be used. For more information, see <a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>.</div><div> </div>

## -parameters

### -param h [in]

A handle to the local memory object. This handle is returned by either the 
<a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-localrealloc">LocalReAlloc</a> function.

## -remarks

Although 
<b>LocalDiscard</b> discards the object's memory block, the handle to the object remains valid. A process can subsequently pass the handle to the 
<a href="/windows/desktop/api/winbase/nf-winbase-localrealloc">LocalReAlloc</a> function to allocate another local memory object identified by the same handle.

## -see-also

<a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localrealloc">LocalReAlloc</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>
