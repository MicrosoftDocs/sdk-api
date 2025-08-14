---
UID: NF:memoryapi.GetProcessWorkingSetSize
tech.root: backup
title: GetProcessWorkingSetSize
ms.date: 06/02/2021
targetos: Windows
description: Retrieves the minimum and maximum working set sizes of the specified process. (GetProcessWorkingSetSize)
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Kernel32.dll
req.header: memoryapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: onecore.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-core-memory-l1-1-9.dll
 - api-ms-win-core-memory-l1-1-8.dll
 - api-ms-win-core-memory-l1-1-7.dll
 - api-ms-win-core-memory-l1-1-6.dll
 - api-ms-win-core-memory-l1-1-5.dll
 - api-ms-win-core-memory-l1-1-4.dll
 - api-ms-win-core-memory-l1-1-3.dll
 - api-ms-win-core-memory-l1-1-2.dll
 - api-ms-win-core-memory-l1-1-1.dll
 - Kernel32.dll
api_name:
 - GetProcessWorkingSetSize
f1_keywords:
 - GetProcessWorkingSetSize
 - memoryapi/GetProcessWorkingSetSize
dev_langs:
 - c++
---

# GetProcessWorkingSetSize function

## -description

Retrieves the minimum and maximum working set sizes of the specified process.

## -parameters

### -param hProcess [in]

A handle to the process whose working set sizes will be obtained. The handle must have the <b>PROCESS_QUERY_INFORMATION</b> or <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right. For more information, see 
<a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the <b>PROCESS_QUERY_INFORMATION</b> access right.

### -param lpMinimumWorkingSetSize [out]

A pointer to a variable that receives the minimum working set size of the specified process, in bytes. The virtual memory manager attempts to keep at least this much memory resident in the process whenever the process is active.

### -param lpMaximumWorkingSetSize [out]

 A pointer to a variable that receives the maximum working set size of the specified process, in bytes. The virtual memory manager attempts to keep no more than this much memory resident in the process whenever the process is active when memory is in short supply.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The "working set" of a process is the set of memory pages currently visible to the process in physical RAM memory. These pages are resident and available for an application to use without triggering a page fault. The minimum and maximum working set sizes affect the virtual memory paging behavior of a process.


#### Examples


```cpp
#include <windows.h>
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[])
{
    SIZE_T  dwMin, dwMax;
    HANDLE hProcess;

    if (argc != 2)
    {
        printf("This program requires a process ID as an argument.\n");
        return 1;
    }

    // Retrieve a handle to the process.

    hProcess = OpenProcess( PROCESS_QUERY_INFORMATION, 
                            FALSE, atoi(argv[1]));
     if (!hProcess)
    {
        printf( "OpenProcess failed (%d)\n", GetLastError() );
        return 1;
    }

    // Retrieve the working set size of the process.

    if (!GetProcessWorkingSetSize(hProcess, &dwMin, &dwMax))
    {
        printf("GetProcessWorkingSetSize failed (%d)\n",
            GetLastError());
        return 1;
    }

    printf("Process ID: %d\n", atoi(argv[1]));
    printf("Minimum working set: %lu KB\n", dwMin/1024);
    printf("Maximum working set: %lu KB\n", dwMax/1024);

    CloseHandle(hProcess);

    return 0;
}

```

## -see-also

[Process Working Set](/windows/desktop/ProcThread/process-working-set)

[Processes](/windows/desktop/ProcThread/child-processes)

[SetProcessWorkingSetSize function](nf-memoryapi-setprocessworkingsetsize.md)

[SetProcessWorkingSetSizeEx function](nf-memoryapi-setprocessworkingsetsizeex.md)
