---
UID: NF:winbase.GlobalAlloc
title: GlobalAlloc function (winbase.h)
description: Allocates the specified number of bytes from the heap. (GlobalAlloc)
helpviewer_keywords: ["GHND","GMEM_FIXED","GMEM_MOVEABLE","GMEM_ZEROINIT","GPTR","GlobalAlloc","GlobalAlloc function","_win32_globalalloc","base.globalalloc","winbase/GlobalAlloc"]
old-location: base\globalalloc.htm
tech.root: base
ms.assetid: 06886545-bd5c-4d81-b1c3-dfa7e146e43a
ms.date: 12/05/2018
ms.keywords: GHND, GMEM_FIXED, GMEM_MOVEABLE, GMEM_ZEROINIT, GPTR, GlobalAlloc, GlobalAlloc function, _win32_globalalloc, base.globalalloc, winbase/GlobalAlloc
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - GlobalAlloc
 - winbase/GlobalAlloc
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
 - API-MS-Win-Core-misc-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-Ms-Win-Core-Heap-L2-1-0.dll
api_name:
 - GlobalAlloc
---

# GlobalAlloc function


## -description

Allocates the specified number of bytes from the heap.
<div class="alert"><b>Note</b>  The global functions have greater overhead and provide fewer features than other memory management functions. New applications should use the 
<a href="/windows/desktop/Memory/heap-functions">heap functions</a> unless documentation states that a global function should be used. For more information, see <a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>.</div><div> </div>

## -parameters

### -param uFlags [in]

The memory allocation attributes. If zero is specified, the default is <b>GMEM_FIXED</b>. This parameter can be one or more of the following values, except for the incompatible combinations that are specifically noted. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GHND"></a><a id="ghnd"></a><dl>
<dt><b>GHND</b></dt>
<dt>0x0042</dt>
</dl>
</td>
<td width="60%">
Combines <b>GMEM_MOVEABLE</b> and <b>GMEM_ZEROINIT</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="GMEM_FIXED"></a><a id="gmem_fixed"></a><dl>
<dt><b>GMEM_FIXED</b></dt>
<dt>0x0000</dt>
</dl>
</td>
<td width="60%">
Allocates fixed memory. The return value is a pointer.

</td>
</tr>
<tr>
<td width="40%"><a id="GMEM_MOVEABLE"></a><a id="gmem_moveable"></a><dl>
<dt><b>GMEM_MOVEABLE</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Allocates movable memory. Memory blocks are never moved in physical memory, but they can be moved within the default heap.

The return value is a handle to the memory object. To translate the handle into a pointer, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-globallock">GlobalLock</a> function.

This value cannot be combined with <b>GMEM_FIXED</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="GMEM_ZEROINIT"></a><a id="gmem_zeroinit"></a><dl>
<dt><b>GMEM_ZEROINIT</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
Initializes memory contents to zero.

</td>
</tr>
<tr>
<td width="40%"><a id="GPTR"></a><a id="gptr"></a><dl>
<dt><b>GPTR</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
Combines <b>GMEM_FIXED</b> and <b>GMEM_ZEROINIT</b>.

</td>
</tr>
</table>
 

The following values are obsolete, but are provided for compatibility with 16-bit Windows. They are ignored.<dl>
<dd><b>GMEM_DDESHARE</b></dd>
<dd><b>GMEM_DISCARDABLE</b></dd>
<dd><b>GMEM_LOWER</b></dd>
<dd><b>GMEM_NOCOMPACT</b></dd>
<dd><b>GMEM_NODISCARD</b></dd>
<dd><b>GMEM_NOT_BANKED</b></dd>
<dd><b>GMEM_NOTIFY</b></dd>
<dd><b>GMEM_SHARE</b></dd>
</dl>

### -param dwBytes [in]

The number of bytes to allocate. If this parameter is zero and the <i>uFlags</i> parameter specifies <b>GMEM_MOVEABLE</b>, the function returns a handle to a memory object that is marked as discarded.

## -returns

If the function succeeds, the return value is a handle to the newly allocated memory object.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Windows memory management does not provide a separate local heap and global heap. Therefore, the <b>GlobalAlloc</b> and <a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> functions are essentially the same. 

The movable-memory flags <b>GHND</b> and <b>GMEM_MOVABLE</b> add unnecessary overhead and require locking to be used safely. They should be avoided unless documentation specifically states that they should be used.

New applications should use the 
<a href="/windows/desktop/Memory/heap-functions">heap functions</a> to allocate and manage memory unless the documentation specifically states that a global function should be used. For example, the global functions are still used with Dynamic Data Exchange (DDE), the clipboard functions, and OLE data objects. 

If the <b>GlobalAlloc</b> function succeeds, it allocates at least the amount of memory requested. If the actual amount allocated is greater than the amount requested, the process can use the entire amount. To determine the actual number of bytes allocated, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-globalsize">GlobalSize</a> function.

If the heap does not contain sufficient free space to satisfy the request, 
<b>GlobalAlloc</b> returns <b>NULL</b>. Because <b>NULL</b> is used to indicate an error, virtual address zero is never allocated. It is, therefore, easy to detect the use of a <b>NULL</b> pointer.

Memory allocated with this function is guaranteed to be aligned on an 8-byte boundary. To execute dynamically generated code, use the <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a> function to allocate memory and the <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualprotect">VirtualProtect</a> function to grant  <b>PAGE_EXECUTE</b> access.

To free the memory, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-globalfree">GlobalFree</a> function. It is not safe to free memory allocated with <b>GlobalAlloc</b> using <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>.


#### Examples

The following code shows a simple use of <b>GlobalAlloc</b> and <a href="/windows/desktop/api/winbase/nf-winbase-globalfree">GlobalFree</a>.


```cpp
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

void _cdecl main()
{
    PSECURITY_DESCRIPTOR pSD;

    pSD = (PSECURITY_DESCRIPTOR) GlobalAlloc(
           GMEM_FIXED,
           sizeof(PSECURITY_DESCRIPTOR));

    // Handle error condition
    if( pSD == NULL )
    {
       _tprintf(TEXT("GlobalAlloc failed (%d)\n"), GetLastError());
       return;
    }

    //see how much memory was allocated
    _tprintf(TEXT("GlobalAlloc allocated %d bytes\n"), GlobalSize(pSD));

    // Use the memory allocated

    // Free the memory when finished with it
    GlobalFree(pSD);
}

```

## -see-also

<a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globaldiscard">GlobalDiscard</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalfree">GlobalFree</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globallock">GlobalLock</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalsize">GlobalSize</a>



<a href="/windows/desktop/Memory/heap-functions">Heap Functions</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory
    Management Functions</a>
