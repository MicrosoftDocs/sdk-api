---
UID: NF:memoryapi.SetProcessValidCallTargets
title: SetProcessValidCallTargets function (memoryapi.h)
description: Provides Control Flow Guard (CFG) with a list of valid indirect call targets and specifies whether they should be marked valid or not.
old-location: base\setprocessvalidcalltargets.htm
tech.root: Memory
ms.assetid: A28BBE75-5188-452B-B784-B6824D4BD161
ms.date: 12/05/2018
ms.keywords: SetProcessValidCallTargets, SetProcessValidCallTargets function, base.setprocessvalidcalltargets, winbase/SetProcessValidCallTargets
f1_keywords:
- memoryapi/SetProcessValidCallTargets
dev_langs:
- c++
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Kernelbase.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- kernelbase.dll
- API-MS-Win-Core-Memory-L1-1-3.dll
- API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
- SetProcessValidCallTargets
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetProcessValidCallTargets function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Provides Control Flow Guard (CFG) with a list of valid indirect call targets and specifies whether they should be marked valid or not. The valid call target information is provided as a list of offsets relative to a virtual memory range

(start and size of the range). The call targets specified should be 16-byte aligned and in ascending

order.


## -parameters




### -param hProcess [in]

The handle to the target process.


### -param VirtualAddress [in]

The start of the virtual memory region whose call targets are being marked valid.


### -param RegionSize [in]

The size of the virtual memory region.


### -param NumberOfOffsets [in]

The number of offsets relative to the virtual memory ranges.


### -param OffsetInformation [in, out]

A list of offsets and flags relative to the virtual memory ranges.


## -returns



<b>TRUE</b> if the operation was successful; otherwise, <b>FALSE</b>. To retrieve error values for this function,  call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.



