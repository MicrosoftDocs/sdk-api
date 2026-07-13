---
UID: NF:sysinfoapi.GlobalMemoryStatusEx
title: GlobalMemoryStatusEx function (sysinfoapi.h)
description: Retrieves information about the system's current usage of both physical and virtual memory. (GlobalMemoryStatusEx)
helpviewer_keywords: ["GlobalMemoryStatusEx","GlobalMemoryStatusEx function","_win32_globalmemorystatusex","base.globalmemorystatusex","sysinfoapi/GlobalMemoryStatusEx"]
old-location: base\globalmemorystatusex.htm
tech.root: base
ms.assetid: bdcee13f-85be-4b9d-b108-3c5ea616dfbb
ms.date: 12/05/2018
ms.keywords: GlobalMemoryStatusEx, GlobalMemoryStatusEx function, _win32_globalmemorystatusex, base.globalmemorystatusex, sysinfoapi/GlobalMemoryStatusEx
req.header: sysinfoapi.h
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
 - GlobalMemoryStatusEx
 - sysinfoapi/GlobalMemoryStatusEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-sysinfo-l1-2-7.dll
 - api-ms-win-core-sysinfo-l1-2-6.dll
 - api-ms-win-core-sysinfo-l1-2-5.dll
 - api-ms-win-core-sysinfo-l1-2-4.dll
 - Kernel32.dll
 - API-MS-Win-Core-SysInfo-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-0.dll
 - API-MS-Win-Core-SysInfo-l1-2-1.dll
 - API-MS-Win-Core-SysInfo-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
 - GlobalMemoryStatusEx
---

# GlobalMemoryStatusEx function


## -description

Retrieves information about the system's current usage of both physical and virtual memory.

## -parameters

### -param lpBuffer [in, out]

A pointer to a 
<a href="/windows/desktop/api/sysinfoapi/ns-sysinfoapi-memorystatusex">MEMORYSTATUSEX</a> structure that receives information about current memory availability.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

You can use the 
<b>GlobalMemoryStatusEx</b> function to determine how much memory your application can allocate without severely impacting other applications.

The information returned by the 
<b>GlobalMemoryStatusEx</b> function is volatile. There is no guarantee that two sequential calls to this function will return the same information.

The  <b>ullAvailPhys</b> member of the <a href="/windows/desktop/api/sysinfoapi/ns-sysinfoapi-memorystatusex">MEMORYSTATUSEX</a> structure at <i>lpBuffer</i> includes memory for all NUMA nodes. 


#### Examples

The following code shows a simple use of the 
<b>GlobalMemoryStatusEx</b> function.


```cpp
//  Sample output:
//  There is       51 percent of memory in use.
//  There are 2029968 total KB of physical memory.
//  There are  987388 free  KB of physical memory.
//  There are 3884620 total KB of paging file.
//  There are 2799776 free  KB of paging file.
//  There are 2097024 total KB of virtual memory.
//  There are 2084876 free  KB of virtual memory.
//  There are       0 free  KB of extended memory.

#include <windows.h>
#include <stdio.h>
#include <tchar.h>

// Use to convert bytes to KB
#define DIV 1024

// Specify the width of the field in which to print the numbers. 
// The asterisk in the format specifier "%*I64d" takes an integer 
// argument and uses it to pad and right justify the number.
#define WIDTH 7

void _tmain()
{
  MEMORYSTATUSEX statex;

  statex.dwLength = sizeof (statex);

  GlobalMemoryStatusEx (&statex);

  _tprintf (TEXT("There is  %*ld percent of memory in use.\n"),
            WIDTH, statex.dwMemoryLoad);
  _tprintf (TEXT("There are %*I64d total KB of physical memory.\n"),
            WIDTH, statex.ullTotalPhys/DIV);
  _tprintf (TEXT("There are %*I64d free  KB of physical memory.\n"),
            WIDTH, statex.ullAvailPhys/DIV);
  _tprintf (TEXT("There are %*I64d total KB of paging file.\n"),
            WIDTH, statex.ullTotalPageFile/DIV);
  _tprintf (TEXT("There are %*I64d free  KB of paging file.\n"),
            WIDTH, statex.ullAvailPageFile/DIV);
  _tprintf (TEXT("There are %*I64d total KB of virtual memory.\n"),
            WIDTH, statex.ullTotalVirtual/DIV);
  _tprintf (TEXT("There are %*I64d free  KB of virtual memory.\n"),
            WIDTH, statex.ullAvailVirtual/DIV);

  // Show the amount of extended memory available.

  _tprintf (TEXT("There are %*I64d free  KB of extended memory.\n"),
            WIDTH, statex.ullAvailExtendedVirtual/DIV);
}

```

## -see-also

<a href="/windows/desktop/api/sysinfoapi/ns-sysinfoapi-memorystatusex">MEMORYSTATUSEX</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory
		  Management Functions</a>



<a href="/previous-versions/windows/desktop/legacy/aa965225(v=vs.85)">Memory Performance Information</a>



<a href="/windows/desktop/Memory/virtual-address-space-and-physical-storage">Virtual Address Space and Physical Storage</a>
