---
UID: NF:winbase.GlobalMemoryStatus
title: GlobalMemoryStatus function (winbase.h)
description: Retrieves information about the system's current usage of both physical and virtual memory. (GlobalMemoryStatus)
helpviewer_keywords: ["GlobalMemoryStatus","GlobalMemoryStatus function","_win32_globalmemorystatus","base.globalmemorystatus","winbase/GlobalMemoryStatus"]
old-location: base\globalmemorystatus.htm
tech.root: base
ms.assetid: 473e4172-b57a-4fc6-9bb2-e916ac3c9a2f
ms.date: 12/05/2018
ms.keywords: GlobalMemoryStatus, GlobalMemoryStatus function, _win32_globalmemorystatus, base.globalmemorystatus, winbase/GlobalMemoryStatus
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GlobalMemoryStatus
 - winbase/GlobalMemoryStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
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
---

# GlobalMemoryStatus function


## -description

<p class="CCE_Message">[<b>GlobalMemoryStatus</b> can return incorrect information. Use the 
<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex">GlobalMemoryStatusEx</a> function instead.]

Retrieves information about the system's current usage of both physical and virtual memory.

## -parameters

### -param lpBuffer [out]

A pointer to a 
<a href="/windows/desktop/api/winbase/ns-winbase-memorystatus">MEMORYSTATUS</a> structure. The 
<b>GlobalMemoryStatus</b> function stores information about current memory availability into this structure.

## -remarks

On computers with more than 4 GB of memory, the 
<b>GlobalMemoryStatus</b> function can return incorrect information, reporting a value of –1 to indicate an overflow. For this reason, applications should use the 
<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex">GlobalMemoryStatusEx</a> function instead.

On Intel x86 computers with more than 2 GB and less than 4 GB of memory, the 
<b>GlobalMemoryStatus</b> function will always return 2 GB in the <b>dwTotalPhys</b> member of the 
<a href="/windows/desktop/api/winbase/ns-winbase-memorystatus">MEMORYSTATUS</a> structure. Similarly, if the total available memory is between 2 and 4 GB, the <b>dwAvailPhys</b> member of the 
<b>MEMORYSTATUS</b> structure will be rounded down to 2 GB. If the executable is linked using the <b>/LARGEADDRESSAWARE</b> linker option, then the 
<b>GlobalMemoryStatus</b> function will return the correct amount of physical memory in both members.

The information returned by the 
<b>GlobalMemoryStatus</b> function is volatile. There is no guarantee that two sequential calls to this function will return the same information.

## -see-also

<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex">GlobalMemoryStatusEx</a>



<a href="/windows/desktop/api/winbase/ns-winbase-memorystatus">MEMORYSTATUS</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>



<a href="/previous-versions/windows/desktop/legacy/aa965225(v=vs.85)">Memory Performance Information</a>



<a href="/windows/desktop/Memory/virtual-address-space-and-physical-storage">Virtual Address Space and Physical Storage</a>
