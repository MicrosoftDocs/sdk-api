---
UID: NF:sysinfoapi.GlobalMemoryStatusEx
title: GlobalMemoryStatusEx function
author: windows-sdk-content
description: Retrieves information about the system's current usage of both physical and virtual memory.
old-location: base\globalmemorystatusex.htm
tech.root: Memory
ms.assetid: bdcee13f-85be-4b9d-b108-3c5ea616dfbb
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GlobalMemoryStatusEx, GlobalMemoryStatusEx function, _win32_globalmemorystatusex, base.globalmemorystatusex, sysinfoapi/GlobalMemoryStatusEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GlobalMemoryStatusEx function


## -description


Retrieves information about the system's current usage of both physical and virtual memory.


## -parameters




### -param lpBuffer [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/ce3c7993-8b91-4bca-8be8-9d81c26b9bef">MEMORYSTATUSEX</a> structure that receives information about current memory availability.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



You can use the 
<b>GlobalMemoryStatusEx</b> function to determine how much memory your application can allocate without severely impacting other applications.

The information returned by the 
<b>GlobalMemoryStatusEx</b> function is volatile. There is no guarantee that two sequential calls to this function will return the same information.

The  <b>ullAvailPhys</b> member of the <a href="https://msdn.microsoft.com/ce3c7993-8b91-4bca-8be8-9d81c26b9bef">MEMORYSTATUSEX</a> structure at <i>lpBuffer</i> includes memory for all NUMA nodes. 


#### Examples

The following code shows a simple use of the 
<b>GlobalMemoryStatusEx</b> function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//  Sample output:
//  There is       51 percent of memory in use.
//  There are 2029968 total KB of physical memory.
//  There are  987388 free  KB of physical memory.
//  There are 3884620 total KB of paging file.
//  There are 2799776 free  KB of paging file.
//  There are 2097024 total KB of virtual memory.
//  There are 2084876 free  KB of virtual memory.
//  There are       0 free  KB of extended memory.

#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;
#include &lt;tchar.h&gt;

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

  GlobalMemoryStatusEx (&amp;statex);

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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ce3c7993-8b91-4bca-8be8-9d81c26b9bef">MEMORYSTATUSEX</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory
		  Management Functions</a>



<a href="https://msdn.microsoft.com/b27ca747-8fd2-4267-9979-4e2e14a5a19f">Memory Performance Information</a>



<a href="https://msdn.microsoft.com/5e8fca7a-b85f-4bbd-80c1-e580a815fdce">Virtual Address Space and Physical Storage</a>
 

 

