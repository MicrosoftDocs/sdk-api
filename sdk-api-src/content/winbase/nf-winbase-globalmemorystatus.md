---
UID: NF:winbase.GlobalMemoryStatus
title: GlobalMemoryStatus function
author: windows-sdk-content
description: Retrieves information about the system's current usage of both physical and virtual memory.
old-location: base\globalmemorystatus.htm
tech.root: Memory
ms.assetid: 473e4172-b57a-4fc6-9bb2-e916ac3c9a2f
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GlobalMemoryStatus, GlobalMemoryStatus function, _win32_globalmemorystatus, base.globalmemorystatus, winbase/GlobalMemoryStatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GlobalMemoryStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GlobalMemoryStatus function


## -description


<p class="CCE_Message">[<b>GlobalMemoryStatus</b> can return incorrect information. Use the 
<a href="https://msdn.microsoft.com/bdcee13f-85be-4b9d-b108-3c5ea616dfbb">GlobalMemoryStatusEx</a> function instead.]

Retrieves information about the system's current usage of both physical and virtual memory.


## -parameters




### -param lpBuffer [out]

A pointer to a 
<a href="https://msdn.microsoft.com/7815ec8f-cacf-4c1b-b5f7-5bb3ef8d759c">MEMORYSTATUS</a> structure. The 
<b>GlobalMemoryStatus</b> function stores information about current memory availability into this structure.


## -returns



This function does not return a value.




## -remarks



On computers with more than 4 GB of memory, the 
<b>GlobalMemoryStatus</b> function can return incorrect information, reporting a value of –1 to indicate an overflow. For this reason, applications should use the 
<a href="https://msdn.microsoft.com/bdcee13f-85be-4b9d-b108-3c5ea616dfbb">GlobalMemoryStatusEx</a> function instead.

On Intel x86 computers with more than 2 GB and less than 4 GB of memory, the 
<b>GlobalMemoryStatus</b> function will always return 2 GB in the <b>dwTotalPhys</b> member of the 
<a href="https://msdn.microsoft.com/7815ec8f-cacf-4c1b-b5f7-5bb3ef8d759c">MEMORYSTATUS</a> structure. Similarly, if the total available memory is between 2 and 4 GB, the <b>dwAvailPhys</b> member of the 
<b>MEMORYSTATUS</b> structure will be rounded down to 2 GB. If the executable is linked using the <b>/LARGEADDRESSAWARE</b> linker option, then the 
<b>GlobalMemoryStatus</b> function will return the correct amount of physical memory in both members.

The information returned by the 
<b>GlobalMemoryStatus</b> function is volatile. There is no guarantee that two sequential calls to this function will return the same information.




## -see-also




<a href="https://msdn.microsoft.com/bdcee13f-85be-4b9d-b108-3c5ea616dfbb">GlobalMemoryStatusEx</a>



<a href="https://msdn.microsoft.com/7815ec8f-cacf-4c1b-b5f7-5bb3ef8d759c">MEMORYSTATUS</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory Management Functions</a>



<a href="https://msdn.microsoft.com/b27ca747-8fd2-4267-9979-4e2e14a5a19f">Memory Performance Information</a>



<a href="https://msdn.microsoft.com/5e8fca7a-b85f-4bbd-80c1-e580a815fdce">Virtual Address Space and Physical Storage</a>
 

 

