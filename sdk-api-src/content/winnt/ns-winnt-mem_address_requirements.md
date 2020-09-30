---
UID: NS:winnt._MEM_ADDRESS_REQUIREMENTS
title: MEM_ADDRESS_REQUIREMENTS (winnt.h)
description: Specifies a lowest and highest base address and alignment as part of an extended parameter to a function that manages virtual memory.
helpviewer_keywords: ["*PMEM_ADDRESS_REQUIREMENTS","MEM_ADDRESS_REQUIREMENTS","MEM_ADDRESS_REQUIREMENTS structure","PMEM_ADDRESS_REQUIREMENTS","PMEM_ADDRESS_REQUIREMENTS structure pointer","base.mem_address_requirements","winnt/MEM_ADDRESS_REQUIREMENTS","winnt/PMEM_ADDRESS_REQUIREMENTS"]
old-location: base\mem_address_requirements.htm
tech.root: base
ms.assetid: 1CAB4942-F0D2-4A60-9472-4EDF2FC9FA7A
ms.date: 12/05/2018
ms.keywords: '*PMEM_ADDRESS_REQUIREMENTS, MEM_ADDRESS_REQUIREMENTS, MEM_ADDRESS_REQUIREMENTS structure, PMEM_ADDRESS_REQUIREMENTS, PMEM_ADDRESS_REQUIREMENTS structure pointer, base.mem_address_requirements, winnt/MEM_ADDRESS_REQUIREMENTS, winnt/PMEM_ADDRESS_REQUIREMENTS'
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MEM_ADDRESS_REQUIREMENTS, *PMEM_ADDRESS_REQUIREMENTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MEM_ADDRESS_REQUIREMENTS
 - winnt/_MEM_ADDRESS_REQUIREMENTS
 - PMEM_ADDRESS_REQUIREMENTS
 - winnt/PMEM_ADDRESS_REQUIREMENTS
 - MEM_ADDRESS_REQUIREMENTS
 - winnt/MEM_ADDRESS_REQUIREMENTS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winnt.h
api_name:
 - MEM_ADDRESS_REQUIREMENTS
---

# MEM_ADDRESS_REQUIREMENTS structure


## -description

Specifies a lowest and highest base address and alignment as part of an extended parameter to a function that manages virtual memory.

## -struct-fields

### -field LowestStartingAddress

Specifies the lowest acceptable address. Calling <a href="https://msdn.microsoft.com/en-us/library/Mt832849(v=VS.85).aspx">VirtualAlloc2</a> or <a href="https://msdn.microsoft.com/en-us/library/Mt832844(v=VS.85).aspx">MapViewOfFile3</a>, and specifying <b>NULL</b> for <i>LowestStartingAddress</i>, gives the same behavior as calling <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a>/<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a>.

### -field HighestEndingAddress

Specifies the highest acceptable address (inclusive). This address must not exceed <b>lpMaximumApplicationAddress</b> returned by <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a>. Calling <a href="https://msdn.microsoft.com/en-us/library/Mt832849(v=VS.85).aspx">VirtualAlloc2</a> or <a href="https://msdn.microsoft.com/en-us/library/Mt832844(v=VS.85).aspx">MapViewOfFile3</a>, and specifying <b>NULL</b> for <i>HighestEndingAddress</i>, gives the same behavior as calling <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a>/<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a>.

### -field Alignment

Specifies power-of-2 alignment. Specifying 0 aligns the returned address on the system allocation granularity.

## -remarks

Specifying a <b>MEM_ADDRESS_REQUIREMENTS</b> structure with all fields set to 0 is the same as not specifying one at all.