---
UID: NF:winbase.GetProcessWorkingSetSize
title: GetProcessWorkingSetSize function (winbase.h)

description: Retrieves the minimum and maximum working set sizes of the specified process.
old-location: base\getprocessworkingsetsize.htm
tech.root: ProcThread
ms.assetid: 9ac2e9ae-31f4-40aa-8d23-6926fa6dec22

ms.date: 12/05/2018
ms.keywords: GetProcessWorkingSetSize, GetProcessWorkingSetSize function, _win32_getprocessworkingsetsize, base.getprocessworkingsetsize, winbase/GetProcessWorkingSetSize
ms.topic: function
f1_keywords: 
 - "winbase/GetProcessWorkingSetSize"
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
 - GetProcessWorkingSetSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetProcessWorkingSetSize function


## -description


Retrieves the minimum and maximum working set sizes of the specified process.


## -parameters




### -param hProcess [in]

A handle to the process whose working set sizes will be obtained. The handle must have the <b>PROCESS_QUERY_INFORMATION</b> or <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the <b>PROCESS_QUERY_INFORMATION</b> access right.


### -param lpMinimumWorkingSetSize [out]

A pointer to a variable that receives the minimum working set size of the specified process, in bytes. The virtual memory manager attempts to keep at least this much memory resident in the process whenever the process is active.


### -param lpMaximumWorkingSetSize [out]

 A pointer to a variable that receives the maximum working set size of the specified process, in bytes. The virtual memory manager attempts to keep no more than this much memory resident in the process whenever the process is active when memory is in short supply.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




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




<a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-working-set">Process Working Set</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/child-processes">Processes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-setprocessworkingsetsize">SetProcessWorkingSetSize</a>
 

 

