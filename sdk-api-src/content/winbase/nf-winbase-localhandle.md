---
UID: NF:winbase.LocalHandle
title: LocalHandle function (winbase.h)
description: Retrieves the handle associated with the specified pointer to a local memory object.
helpviewer_keywords: ["LocalHandle","LocalHandle function","_win32_localhandle","base.localhandle","winbase/LocalHandle"]
old-location: base\localhandle.htm
tech.root: base
ms.assetid: 2b252f8b-d0a3-4d7f-9e2e-cb80c1512935
ms.date: 12/05/2018
ms.keywords: LocalHandle, LocalHandle function, _win32_localhandle, base.localhandle, winbase/LocalHandle
f1_keywords:
- winbase/LocalHandle
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Kernel32.dll
api_name:
- LocalHandle
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LocalHandle function


## -description


Retrieves the handle associated with the specified pointer to a local memory object.
<div class="alert"><b>Note</b>  The local functions have greater overhead and provide fewer features than other memory management functions. New applications should use the <a href="https://docs.microsoft.com/windows/desktop/Memory/heap-functions">heap functions</a> unless documentation states that a local function should be used. For more information, see <a href="https://docs.microsoft.com/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>.</div><div> </div>

## -parameters




### -param pMem [in]

A pointer to the first byte of the local memory object. This pointer is returned by the 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-locallock">LocalLock</a> function.


## -returns



If the function succeeds, the return value is a handle to the specified local memory object.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



When the 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> function allocates a local memory object with <b>LMEM_MOVEABLE</b>, it returns a handle to the object. The 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-locallock">LocalLock</a> function converts this handle into a pointer to the object's memory block, and 
<b>LocalHandle</b> converts the pointer back into a handle.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-locallock">LocalLock</a>



<a href="https://docs.microsoft.com/windows/desktop/Memory/memory-management-functions">Memory
    Management Functions</a>
 

 

