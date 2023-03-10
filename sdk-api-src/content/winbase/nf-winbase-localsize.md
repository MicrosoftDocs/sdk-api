---
UID: NF:winbase.LocalSize
title: LocalSize function (winbase.h)
description: Retrieves the current size of the specified local memory object, in bytes.
helpviewer_keywords: ["LocalSize","LocalSize function","_win32_localsize","base.localsize","winbase/LocalSize"]
old-location: base\localsize.htm
tech.root: base
ms.assetid: d1337845-d89c-4cd5-a584-36fe0c682c1a
ms.date: 12/05/2018
ms.keywords: LocalSize, LocalSize function, _win32_localsize, base.localsize, winbase/LocalSize
req.header: winbase.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LocalSize
 - winbase/LocalSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Heap-Obsolete-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
api_name:
 - LocalSize
---

# LocalSize function


## -description

Retrieves the current size of the specified local memory object, in bytes.
<div class="alert"><b>Note</b>  The local functions have greater overhead and provide fewer features than other memory management functions. New applications should use the <a href="/windows/desktop/Memory/heap-functions">heap functions</a> unless documentation states that a local function should be used. For more information, see <a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>.</div><div> </div>

## -parameters

### -param hMem [in]

A handle to the local memory object. This handle is returned by the 
<a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a>, 
<a href="/windows/desktop/api/winbase/nf-winbase-localrealloc">LocalReAlloc</a>, or 
<a href="/windows/desktop/api/winbase/nf-winbase-localhandle">LocalHandle</a> function.

## -returns

If the function succeeds, the return value is the size of the specified local memory object, in bytes. If the specified handle is not valid or if the object has been discarded, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The size of a memory block may be larger than the size requested when the memory was allocated.

To verify that the specified object's memory block has not been discarded, call the 
<a href="/windows/desktop/api/winbase/nf-winbase-localflags">LocalFlags</a> function before calling 
<b>LocalSize</b>.

## -see-also

<a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localflags">LocalFlags</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localhandle">LocalHandle</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localrealloc">LocalReAlloc</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory
		  Management Functions</a>