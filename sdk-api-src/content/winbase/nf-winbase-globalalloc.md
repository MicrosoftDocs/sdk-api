---
UID: NF:winbase.GlobalAlloc
title: GlobalAlloc function
author: windows-sdk-content
description: Allocates the specified number of bytes from the heap.
old-location: base\globalalloc.htm
tech.root: Memory
ms.assetid: 06886545-bd5c-4d81-b1c3-dfa7e146e43a
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GHND, GMEM_FIXED, GMEM_MOVEABLE, GMEM_ZEROINIT, GPTR, GlobalAlloc, GlobalAlloc function, _win32_globalalloc, base.globalalloc, winbase/GlobalAlloc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GlobalAlloc function


## -description


Allocates the specified number of bytes from the heap.
<div class="alert"><b>Note</b>  The global functions have greater overhead and provide fewer features than other memory management functions. New applications should use the 
<a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">heap functions</a> unless documentation states that a global function should be used. For more information, see <a href="https://msdn.microsoft.com/97707ce7-4c65-4d0e-ba69-47fdaee73a9b">Global and Local Functions</a>.</div><div> </div>

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
<a href="https://msdn.microsoft.com/0d7deac2-c9c4-4adc-8a0a-edfc512a4d6c">GlobalLock</a> function.

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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Windows memory management does not provide a separate local heap and global heap. Therefore, the <b>GlobalAlloc</b> and <a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a> functions are essentially the same. 

The movable-memory flags <b>GHND</b> and <b>GMEM_MOVABLE</b> add unnecessary overhead and require locking to be used safely. They should be avoided unless documentation specifically states that they should be used.

New applications should use the 
<a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">heap functions</a> to allocate and manage memory unless the documentation specifically states that a global function should be used. For example, the global functions are still used with Dynamic Data Exchange (DDE), the clipboard functions, and OLE data objects. 

If the <b>GlobalAlloc</b> function succeeds, it allocates at least the amount of memory requested. If the actual amount allocated is greater than the amount requested, the process can use the entire amount. To determine the actual number of bytes allocated, use the 
<a href="https://msdn.microsoft.com/9fd01460-d6fc-41f4-9e0c-209a3d1844c1">GlobalSize</a> function.

If the heap does not contain sufficient free space to satisfy the request, 
<b>GlobalAlloc</b> returns <b>NULL</b>. Because <b>NULL</b> is used to indicate an error, virtual address zero is never allocated. It is, therefore, easy to detect the use of a <b>NULL</b> pointer.

Memory allocated with this function is guaranteed to be aligned on an 8-byte boundary. To execute dynamically generated code, use the <a href="https://msdn.microsoft.com/a720dd89-c47c-4e48-bbc6-f2e02dfc4ed2">VirtualAlloc</a> function to allocate memory and the <a href="https://msdn.microsoft.com/a0018bba-226b-4c18-8ea4-15e69524db11">VirtualProtect</a> function to grant  <b>PAGE_EXECUTE</b> access.

To free the memory, use the 
<a href="https://msdn.microsoft.com/5fe910ac-f857-45ca-9c0f-4f9ba3c5e61b">GlobalFree</a> function. It is not safe to free memory allocated with <b>GlobalAlloc</b> using <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>.


#### Examples

The following code shows a simple use of <b>GlobalAlloc</b> and <a href="https://msdn.microsoft.com/5fe910ac-f857-45ca-9c0f-4f9ba3c5e61b">GlobalFree</a>.


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




<a href="https://msdn.microsoft.com/97707ce7-4c65-4d0e-ba69-47fdaee73a9b">Global and Local Functions</a>



<a href="https://msdn.microsoft.com/af6160ce-ab7a-4198-bca3-dd5d51cacfa5">GlobalDiscard</a>



<a href="https://msdn.microsoft.com/5fe910ac-f857-45ca-9c0f-4f9ba3c5e61b">GlobalFree</a>



<a href="https://msdn.microsoft.com/0d7deac2-c9c4-4adc-8a0a-edfc512a4d6c">GlobalLock</a>



<a href="https://msdn.microsoft.com/9fd01460-d6fc-41f4-9e0c-209a3d1844c1">GlobalSize</a>



<a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">Heap Functions</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory
    Management Functions</a>
 

 

