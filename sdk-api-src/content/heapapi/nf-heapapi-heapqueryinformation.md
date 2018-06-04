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

# HeapQueryInformation function


## -description


Retrieves information about the specified heap.


## -parameters




### -param HeapHandle [in, optional]

A handle to the heap whose information is to be retrieved. This handle is returned by either the 
<a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a> or 
<a href="https://msdn.microsoft.com/ecd716b2-df48-4914-9de4-47d8ad8ff9a2">GetProcessHeap</a> function.


### -param HeapInformationClass [in]

The class of information to be retrieved. This parameter can be the following value from the <b>HEAP_INFORMATION_CLASS</b> enumeration type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HeapCompatibilityInformation"></a><a id="heapcompatibilityinformation"></a><a id="HEAPCOMPATIBILITYINFORMATION"></a><dl>
<dt><b>HeapCompatibilityInformation</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Indicates the heap features that are enabled. 




The <i>HeapInformation</i> parameter is a pointer to a <b>ULONG</b> variable.

If <i>HeapInformation</i> is 0, the heap is a standard heap that does not support look-aside lists.

If <i>HeapInformation</i> is 1, the heap supports look-aside lists. For more information, see Remarks.

If <i>HeapInformation</i> is 2, the <a href="https://msdn.microsoft.com/d10abf82-423c-4942-b05e-55de3a5c4219">low-fragmentation heap</a> (LFH) has been enabled for the heap. Enabling the LFH disables look-aside lists.

</td>
</tr>
</table>
 


### -param HeapInformation [out]

A pointer to a buffer that receives the heap information. The format of this data depends on the value of the <i>HeapInformationClass</i> parameter.


### -param HeapInformationLength [in]

The size of the heap information being queried, in bytes.


### -param ReturnLength [out, optional]

A pointer to a variable that receives the length of data written to the <i>HeapInformation</i> buffer. If the buffer is too small, the function fails and <i>ReturnLength</i> specifies the minimum size required for the buffer. 




If you do not want to receive this information, specify <b>NULL</b>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To enable the 
LFH or the terminate-on-corruption feature, use the 
<a href="https://msdn.microsoft.com/33c262ca-5093-4f44-a8c6-09045bc90f60">HeapSetInformation</a> function.

<b>Windows XP and Windows Server 2003:  </b> A look-aside list is a fast memory allocation mechanism that contains only fixed-sized blocks. Look-aside lists are enabled by default for heaps that support them. Starting with Windows Vista, look-aside lists are not used and the LFH is enabled by default.

Look-aside lists are faster than general pool allocations that vary in size, because the system does not search for free memory that fits the allocation. In addition, access to look-aside lists is generally synchronized using fast atomic processor exchange instructions instead of mutexes or spinlocks. Look-aside lists can be created by the system or drivers. They can be allocated from paged or nonpaged pool. 






#### Examples

The following example uses <a href="https://msdn.microsoft.com/ecd716b2-df48-4914-9de4-47d8ad8ff9a2">GetProcessHeap</a> to 
     obtain a handle to the default process heap and 
     <b>HeapQueryInformation</b> to retrieve information 
     about the heap.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;tchar.h&gt;
#include &lt;stdio.h&gt;

#define HEAP_STANDARD 0
#define HEAP_LAL 1
#define HEAP_LFH 2

int __cdecl _tmain()
{
    BOOL bResult;
    HANDLE hHeap;
    ULONG HeapInformation;

    //
    // Get a handle to the default process heap.
    //
    hHeap = GetProcessHeap();
    if (hHeap == NULL) {
        _tprintf(TEXT("Failed to retrieve default process heap with LastError %d.\n"),
                 GetLastError());
        return 1;
    }

    //
    // Query heap features that are enabled.
    //
    bResult = HeapQueryInformation(hHeap,
                                   HeapCompatibilityInformation,
                                   &amp;HeapInformation,
                                   sizeof(HeapInformation),
                                   NULL);
    if (bResult == FALSE) {
        _tprintf(TEXT("Failed to retrieve heap features with LastError %d.\n"),
                 GetLastError());
        return 1;
    }

    //
    // Print results of the query.
    //
    _tprintf(TEXT("HeapCompatibilityInformation is %d.\n"), HeapInformation);
    switch(HeapInformation)
    {
    case HEAP_STANDARD:
        _tprintf(TEXT("The default process heap is a standard heap.\n"));
        break;
    case HEAP_LAL:
        _tprintf(TEXT("The default process heap supports look-aside lists.\n"));
        break;
    case HEAP_LFH:
        _tprintf(TEXT("The default process heap has the low-fragmentation ") \
                 TEXT("heap enabled.\n"));
        break;
    default:
        _tprintf(TEXT("Unrecognized HeapInformation reported for the default ") \
                 TEXT("process heap.\n"));
        break;
     }

    return 0;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ecd716b2-df48-4914-9de4-47d8ad8ff9a2">GetProcessHeap</a>



<a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">Heap Functions</a>



<a href="https://msdn.microsoft.com/8c0a77a2-37e6-41f7-bdc6-1f3768d61c9b">HeapCreate</a>



<a href="https://msdn.microsoft.com/33c262ca-5093-4f44-a8c6-09045bc90f60">HeapSetInformation</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory Management Functions</a>
 

 

