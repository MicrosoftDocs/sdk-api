---
UID: NF:heapapi.HeapSize
title: HeapSize function
author: windows-sdk-content
description: Retrieves the size of a memory block allocated from a heap by the HeapAlloc or HeapReAlloc function.
old-location: base\heapsize.htm
old-project: memory
ms.assetid: a8fcfd99-7b04-4aa3-8619-272b254551a3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: HEAP_NO_SERIALIZE, HeapSize, HeapSize function, _win32_heapsize, base.heapsize, heapapi/HeapSize, winbase/HeapSize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: heapapi.h
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
tech.root: 
req.typenames: GPMStarterGPOType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-heap-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-heap-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - HeapSize
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: GDI+ 1.1
---

# HeapSize function


## -description


Retrieves the size of a memory block allocated from a heap by the 
    <a href="https://msdn.microsoft.com/9a176312-0312-4cc1-baf5-949b346d983e">HeapAlloc</a> or 
    <a href="https://msdn.microsoft.com/21d711d9-3b16-4537-a830-1a2fa049a471">HeapReAlloc</a> function.


## -parameters




### -param hHeap [in]

A handle to the heap in which the memory block resides. This handle is returned by either the 
      <a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a> or 
      <a href="https://msdn.microsoft.com/ecd716b2-df48-4914-9de4-47d8ad8ff9a2">GetProcessHeap</a> function.


### -param dwFlags [in]

The heap size options. Specifying the following value overrides the corresponding value specified in the 
      <i>flOptions</i> parameter when the heap was created by using the 
      <a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a> function.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HEAP_NO_SERIALIZE"></a><a id="heap_no_serialize"></a><dl>
<dt><b>HEAP_NO_SERIALIZE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Serialized access will not be used. For more information, see Remarks.

To ensure that serialized access is disabled for all calls to this function, specify 
         <b>HEAP_NO_SERIALIZE</b> in the call to 
         <a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a>. In this case, it is not necessary to 
         additionally specify <b>HEAP_NO_SERIALIZE</b> in this function call.

This value should not be specified when accessing the process heap. The system may create additional 
         threads within the application's process, such as a CTRL+C handler, that simultaneously access the process 
         heap.

</td>
</tr>
</table>
 


### -param lpMem [in]

A pointer to the memory block whose size the function will obtain. This is a pointer returned by the 
      <a href="https://msdn.microsoft.com/9a176312-0312-4cc1-baf5-949b346d983e">HeapAlloc</a> or 
      <a href="https://msdn.microsoft.com/21d711d9-3b16-4537-a830-1a2fa049a471">HeapReAlloc</a> function. The memory block must 
      be from the heap specified by the <i>hHeap</i> parameter.


## -returns



If the function succeeds, the return value is the requested size of the allocated memory block, in bytes.

If the function fails, the return value is <code>(SIZE_T)-1</code>. 
       The function does not call <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a>. An 
       application cannot call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> for extended 
       error information.

If the <i>lpMem</i> parameter refers to a heap allocation that is not in the heap 
       specified by the <i>hHeap</i> parameter, the behavior of the 
       <b>HeapSize</b> function is undefined.




## -remarks



Serialization ensures mutual exclusion when two or more threads attempt to simultaneously allocate or free 
    blocks from the same heap. There is a small performance cost to serialization, but it must be used whenever 
    multiple threads allocate and free memory from the same heap. Setting the 
    <b>HEAP_NO_SERIALIZE</b> value eliminates mutual exclusion on the heap. Without serialization, 
    two or more threads that use the same heap handle might attempt to allocate or free memory simultaneously, likely 
    causing corruption in the heap. The <b>HEAP_NO_SERIALIZE</b> value can, therefore, be safely 
    used only in the following situations:

<ul>
<li>The process has only one thread.</li>
<li>The process has multiple threads, but only one thread calls the heap functions for a specific heap.</li>
<li>The process has multiple threads, and the application provides its own mechanism for mutual exclusion to a 
      specific heap.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">Heap Functions</a>



<a href="https://msdn.microsoft.com/9a176312-0312-4cc1-baf5-949b346d983e">HeapAlloc</a>



<a href="https://msdn.microsoft.com/21d711d9-3b16-4537-a830-1a2fa049a471">HeapReAlloc</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory Management Functions</a>
 

 

