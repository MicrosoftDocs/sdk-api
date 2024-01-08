---
UID: NF:heapapi.HeapSetInformation
title: HeapSetInformation function (heapapi.h)
description: Enables features for a specified heap.
helpviewer_keywords: ["HeapCompatibilityInformation","HeapEnableTerminationOnCorruption","HeapOptimizeResources","HeapSetInformation","HeapSetInformation function","_win32_heapsetinformation","base.heapsetinformation","heapapi/HeapSetInformation","winbase/HeapSetInformation"]
old-location: base\heapsetinformation.htm
tech.root: base
ms.assetid: 33c262ca-5093-4f44-a8c6-09045bc90f60
ms.date: 12/05/2018
ms.keywords: HeapCompatibilityInformation, HeapEnableTerminationOnCorruption, HeapOptimizeResources, HeapSetInformation, HeapSetInformation function, _win32_heapsetinformation, base.heapsetinformation, heapapi/HeapSetInformation, winbase/HeapSetInformation
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HeapSetInformation
 - heapapi/HeapSetInformation
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
 - HeapSetInformation
---

# HeapSetInformation function


## -description

Enables features for a specified heap.

## -parameters

### -param HeapHandle [in, optional]

A handle to the heap where information is to be set. This handle is returned by either the 
      <a href="/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a> or 
      <a href="/windows/desktop/api/heapapi/nf-heapapi-getprocessheap">GetProcessHeap</a> function.

### -param HeapInformationClass [in]

The class of information to be set. This parameter can be one of the following values from the 
      <b>HEAP_INFORMATION_CLASS</b> enumeration type.

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
Enables heap features. Only the 
        <a href="/windows/desktop/Memory/low-fragmentation-heap">low-fragmentation heap</a> (LFH) is supported. 
        However, it is not necessary for applications to enable the LFH because the system uses the LFH as needed to 
        service memory allocation requests.
        

<b>Windows XP and Windows Server 2003:  </b>The LFH is not enabled by default. To enable the LFH for the specified heap, set the variable pointed to 
           by the <i>HeapInformation</i> parameter to 2. After the LFH is enabled for a heap, it 
           cannot be disabled.

The LFH cannot be enabled for heaps created with <b>HEAP_NO_SERIALIZE</b> or for heaps 
           created with a fixed size. The LFH also cannot be enabled if you are using the heap debugging tools in 
           <a href="/windows-hardware/drivers/debugger/">Debugging Tools for Windows</a> 
           or 
           <a href="/windows-hardware/drivers/devtest/application-verifier">Microsoft Application Verifier</a>.

When a process is run under any debugger, certain heap debug options are automatically enabled for all 
           heaps in the process. These heap debug options prevent the use of the LFH. To enable the low-fragmentation 
           heap when running under a debugger, set the _NO_DEBUG_HEAP environment variable 
           to 1.



</td>
</tr>
<tr>
<td width="40%"><a id="HeapEnableTerminationOnCorruption"></a><a id="heapenableterminationoncorruption"></a><a id="HEAPENABLETERMINATIONONCORRUPTION"></a><dl>
<dt><b>HeapEnableTerminationOnCorruption</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Enables the terminate-on-corruption feature. If the heap manager detects an error in any heap used by the 
         process, it calls the Windows Error Reporting service and terminates the process.

After a process enables this feature, it cannot be disabled.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Vista and Windows XP with SP3. The 
          function succeeds but the <b>HeapEnableTerminationOnCorruption</b> value is 
          ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="HeapOptimizeResources"></a><a id="heapoptimizeresources"></a><a id="HEAPOPTIMIZERESOURCES"></a><dl>
<dt><b>HeapOptimizeResources</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
If HeapSetInformation is called with <i>HeapHandle</i> set to NULL, then all heaps in the process with a <a href="/windows/desktop/Memory/low-fragmentation-heap">low-fragmentation heap</a> (LFH) will have their caches optimized,  and the memory will be decommitted if possible.  

If a heap pointer is supplied in <i>HeapHandle</i>, then only that heap will be optimized.

Note that the HEAP_OPTIMIZE_RESOURCES_INFORMATION  structure passed in <i>HeapInformation</i> must be properly initialized.

<b>Note</b>  This value was added in Windows 8.1. 

</td>
</tr>
</table>

### -param HeapInformation [in]

The heap information buffer. The format of this data depends on the value of the 
       <i>HeapInformationClass</i> parameter.

If the <i>HeapInformationClass</i> parameter is 
       <b>HeapCompatibilityInformation</b>, the <i>HeapInformation</i> 
       parameter is a pointer to a <b>ULONG</b> variable.

If the <i>HeapInformationClass</i> parameter is 
       <b>HeapEnableTerminationOnCorruption</b>, the <i>HeapInformation</i> 
       parameter should be <b>NULL</b> and <i>HeapInformationLength</i> should 
       be 0

### -param HeapInformationLength [in]

The size of the <i>HeapInformation</i> buffer, in bytes.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To retrieve the current settings for the heap, use the 
    <a href="/windows/desktop/api/heapapi/nf-heapapi-heapqueryinformation">HeapQueryInformation</a> function.

Setting the <b>HeapEnableTerminateOnCorruption</b> option is strongly recommended because 
    it reduces an application's exposure to security exploits that take advantage of a corrupted heap.


#### Examples

The following example shows you how to enable the low-fragmentation heap.


```cpp
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define HEAP_LFH 2

int __cdecl _tmain()
{
    BOOL bResult;
    HANDLE hHeap;
    ULONG HeapInformation;

    //
    // Enable heap terminate-on-corruption. 
    // A correct application can continue to run even if this call fails, 
    // so it is safe to ignore the return value and call the function as follows:
    // (void)HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);
    // If the application requires heap terminate-on-corruption to be enabled, 
    // check the return value and exit on failure as shown in this example.
    //
    bResult = HeapSetInformation(NULL,
                                 HeapEnableTerminationOnCorruption,
                                 NULL,
                                 0);

    if (bResult != FALSE) {
        _tprintf(TEXT("Heap terminate-on-corruption has been enabled.\n"));
    }
    else {
        _tprintf(TEXT("Failed to enable heap terminate-on-corruption with LastError %d.\n"),
                 GetLastError());
        return 1;
    }

    //
    // Create a new heap with default parameters.
    //
    hHeap = HeapCreate(0, 0, 0);
    if (hHeap == NULL) {
        _tprintf(TEXT("Failed to create a new heap with LastError %d.\n"),
                 GetLastError());
        return 1;
    }

    //
    // Enable the low-fragmentation heap (LFH). Starting with Windows Vista, 
    // the LFH is enabled by default but this call does not cause an error.
    //
    HeapInformation = HEAP_LFH;
    bResult = HeapSetInformation(hHeap,
                                 HeapCompatibilityInformation,
                                 &HeapInformation,
                                 sizeof(HeapInformation));
    if (bResult != FALSE) {
        _tprintf(TEXT("The low-fragmentation heap has been enabled.\n"));
    }
    else {
        _tprintf(TEXT("Failed to enable the low-fragmentation heap with LastError %d.\n"),
                 GetLastError());
        return 1;
    }

    return 0;
}

```

## -see-also

<a href="/windows/desktop/api/heapapi/nf-heapapi-getprocessheap">GetProcessHeap</a>



<a href="/windows/desktop/Memory/heap-functions">Heap Functions</a>



<a href="/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a>



<a href="/windows/desktop/api/heapapi/nf-heapapi-heapqueryinformation">HeapQueryInformation</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>