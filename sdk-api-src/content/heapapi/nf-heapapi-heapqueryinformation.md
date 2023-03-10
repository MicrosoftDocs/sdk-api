---
UID: NF:heapapi.HeapQueryInformation
title: HeapQueryInformation function (heapapi.h)
description: Retrieves information about the specified heap.
helpviewer_keywords: ["HeapCompatibilityInformation","HeapQueryInformation","HeapQueryInformation function","_win32_heapqueryinformation","base.heapqueryinformation","heapapi/HeapQueryInformation","winbase/HeapQueryInformation"]
old-location: base\heapqueryinformation.htm
tech.root: base
ms.assetid: 6bf6cb8b-7212-4ddb-9ea6-34bc78824a8f
ms.date: 12/05/2018
ms.keywords: HeapCompatibilityInformation, HeapQueryInformation, HeapQueryInformation function, _win32_heapqueryinformation, base.heapqueryinformation, heapapi/HeapQueryInformation, winbase/HeapQueryInformation
req.header: heapapi.h
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
 - HeapQueryInformation
 - heapapi/HeapQueryInformation
dev_langs:
 - c++
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
 - HeapQueryInformation
---

# HeapQueryInformation function


## -description

Retrieves information about the specified heap.

## -parameters

### -param HeapHandle [in, optional]

A handle to the heap whose information is to be retrieved. This handle is returned by either the 
<a href="/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a> or 
<a href="/windows/desktop/api/heapapi/nf-heapapi-getprocessheap">GetProcessHeap</a> function.

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

If <i>HeapInformation</i> is 2, the <a href="/windows/desktop/Memory/low-fragmentation-heap">low-fragmentation heap</a> (LFH) has been enabled for the heap. Enabling the LFH disables look-aside lists.

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
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To enable the 
LFH or the terminate-on-corruption feature, use the 
<a href="/windows/desktop/api/heapapi/nf-heapapi-heapsetinformation">HeapSetInformation</a> function.

<b>Windows XP and Windows Server 2003:  </b> A look-aside list is a fast memory allocation mechanism that contains only fixed-sized blocks. Look-aside lists are enabled by default for heaps that support them. Starting with Windows Vista, look-aside lists are not used and the LFH is enabled by default.

Look-aside lists are faster than general pool allocations that vary in size, because the system does not search for free memory that fits the allocation. In addition, access to look-aside lists is generally synchronized using fast atomic processor exchange instructions instead of mutexes or spinlocks. Look-aside lists can be created by the system or drivers. They can be allocated from paged or nonpaged pool. 






#### Examples

The following example uses <a href="/windows/desktop/api/heapapi/nf-heapapi-getprocessheap">GetProcessHeap</a> to 
     obtain a handle to the default process heap and 
     <b>HeapQueryInformation</b> to retrieve information 
     about the heap.


```cpp
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

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
                                   &HeapInformation,
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

```

## -see-also

<a href="/windows/desktop/api/heapapi/nf-heapapi-getprocessheap">GetProcessHeap</a>



<a href="/windows/desktop/Memory/heap-functions">Heap Functions</a>



<a href="/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a>



<a href="/windows/desktop/api/heapapi/nf-heapapi-heapsetinformation">HeapSetInformation</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>