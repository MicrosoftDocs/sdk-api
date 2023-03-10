---
UID: NF:winbase.LocalAlloc
title: LocalAlloc function (winbase.h)
description: Allocates the specified number of bytes from the heap. (LocalAlloc)
helpviewer_keywords: ["LHND","LMEM_FIXED","LMEM_MOVEABLE","LMEM_ZEROINIT","LPTR","LocalAlloc","LocalAlloc function","NONZEROLHND","NONZEROLPTR","_win32_localalloc","base.localalloc","winbase/LocalAlloc"]
old-location: base\localalloc.htm
tech.root: base
ms.assetid: da8cd2be-ff4c-4da5-813c-8759a58228c9
ms.date: 12/05/2018
ms.keywords: LHND, LMEM_FIXED, LMEM_MOVEABLE, LMEM_ZEROINIT, LPTR, LocalAlloc, LocalAlloc function, NONZEROLHND, NONZEROLPTR, _win32_localalloc, base.localalloc, winbase/LocalAlloc
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
 - LocalAlloc
 - winbase/LocalAlloc
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
 - LocalAlloc
---

# LocalAlloc function


## -description

Allocates the specified number of bytes from the heap.
<div class="alert"><b>Note</b>  The local functions have greater overhead and provide fewer features than other memory management functions. New applications should use the 
<a href="/windows/desktop/Memory/heap-functions">heap functions</a> unless documentation states that a local function should be used. For more information, see <a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>.</div><div> </div>

## -parameters

### -param uFlags [in]

The memory allocation attributes. The default is the <b>LMEM_FIXED</b> value. This parameter can be one or more of the following values, except for the incompatible combinations that are specifically noted. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LHND"></a><a id="lhnd"></a><dl>
<dt><b>LHND</b></dt>
<dt>0x0042</dt>
</dl>
</td>
<td width="60%">
Combines <b>LMEM_MOVEABLE</b> and <b>LMEM_ZEROINIT</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="LMEM_FIXED"></a><a id="lmem_fixed"></a><dl>
<dt><b>LMEM_FIXED</b></dt>
<dt>0x0000</dt>
</dl>
</td>
<td width="60%">
Allocates fixed memory. The return value is a pointer to the memory object.

</td>
</tr>
<tr>
<td width="40%"><a id="LMEM_MOVEABLE"></a><a id="lmem_moveable"></a><dl>
<dt><b>LMEM_MOVEABLE</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Allocates movable memory. Memory blocks are never moved in physical memory, but they can be moved within the default heap. 




The return value is a handle to the memory object. To translate the handle to a pointer, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-locallock">LocalLock</a> function.

This value cannot be combined with <b>LMEM_FIXED</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="LMEM_ZEROINIT"></a><a id="lmem_zeroinit"></a><dl>
<dt><b>LMEM_ZEROINIT</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
Initializes memory contents to zero.

</td>
</tr>
<tr>
<td width="40%"><a id="LPTR"></a><a id="lptr"></a><dl>
<dt><b>LPTR</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
Combines <b>LMEM_FIXED</b> and <b>LMEM_ZEROINIT</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="NONZEROLHND"></a><a id="nonzerolhnd"></a><dl>
<dt><b>NONZEROLHND</b></dt>
</dl>
</td>
<td width="60%">
Same as <b>LMEM_MOVEABLE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="NONZEROLPTR"></a><a id="nonzerolptr"></a><dl>
<dt><b>NONZEROLPTR</b></dt>
</dl>
</td>
<td width="60%">
Same as <b>LMEM_FIXED</b>.

</td>
</tr>
</table>
 

The following values are obsolete, but are provided for compatibility with 16-bit Windows. They are ignored.<dl>
<dd><b>LMEM_DISCARDABLE</b></dd>
<dd><b>LMEM_NOCOMPACT</b></dd>
<dd><b>LMEM_NODISCARD</b></dd>
</dl>

### -param uBytes [in]

The number of bytes to allocate. If this parameter is zero and the <i>uFlags</i> parameter specifies <b>LMEM_MOVEABLE</b>, the function returns a handle to a memory object that is marked as discarded.

## -returns

If the function succeeds, the return value is a handle to the newly allocated memory object.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Windows memory management does not provide a separate local heap and global heap. Therefore, the <b>LocalAlloc</b> and <a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a> functions are essentially the same. 

The movable-memory flags <b>LHND</b>, <b>LMEM_MOVABLE</b>, and <b>NONZEROLHND</b> add unnecessary overhead and require locking to be used safely. They should be avoided unless documentation specifically states that they should be used.

New applications should use the 
<a href="/windows/desktop/Memory/heap-functions">heap functions</a> unless the documentation specifically states that a local function should be used. For example, some Windows functions allocate memory that must be freed with <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>.

If the heap does not contain sufficient free space to satisfy the request, 
<b>LocalAlloc</b> returns <b>NULL</b>. Because <b>NULL</b> is used to indicate an error, virtual address zero is never allocated. It is, therefore, easy to detect the use of a <b>NULL</b> pointer.

If the <b>LocalAlloc</b> function succeeds, it allocates at least the amount requested. If the amount allocated is greater than the amount requested, the process can use the entire amount. To determine the actual number of bytes allocated, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-localsize">LocalSize</a> function.

To free the memory, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function. It is not safe to free memory allocated with <b>LocalAlloc</b> using <a href="/windows/desktop/api/winbase/nf-winbase-globalfree">GlobalFree</a>.


#### Examples

The following code shows a simple use of <b>LocalAlloc</b> and <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>.


```cpp
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

void _cdecl _tmain()
{
    LPTSTR pszBuf=NULL;

    pszBuf = (LPTSTR)LocalAlloc(
              LPTR,
              MAX_PATH*sizeof(TCHAR));

    // Handle error condition
    if( pszBuf == NULL )
    {
       _tprintf(TEXT("LocalAlloc failed (%d)\n"), GetLastError());
       return;
    }

    //see how much memory was allocated
    _tprintf(TEXT("LocalAlloc allocated %d bytes\n"), LocalSize(pszBuf));

    // Use the memory allocated

    // Free the memory when finished with it
    LocalFree(pszBuf);
}

```

## -see-also

<a href="/windows/desktop/Memory/global-and-local-functions">Global and Local Functions</a>



<a href="/windows/desktop/Memory/heap-functions">Heap Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>



<a href="/windows/desktop/api/winbase/nf-winbase-locallock">LocalLock</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localrealloc">LocalReAlloc</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localsize">LocalSize</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory
    Management Functions</a>
