---
UID: NF:winddi.EngFreeMem
title: EngFreeMem macro (winddi.h)
description: The EngFreeMem function deallocates a block of system memory.
helpviewer_keywords: ["EngFreeMem","EngFreeMem function [Display Devices]","display.engfreemem","gdifncs_4479237b-46a6-40a1-a9ad-dd1cd0a4c4bb.xml","winddi/EngFreeMem"]
old-location: display\engfreemem.htm
tech.root: display
ms.assetid: 04428d7e-4150-4e68-a660-0a9e246c82ae
ms.date: 12/05/2018
ms.keywords: EngFreeMem, EngFreeMem function [Display Devices], display.engfreemem, gdifncs_4479237b-46a6-40a1-a9ad-dd1cd0a4c4bb.xml, winddi/EngFreeMem
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngFreeMem
 - winddi/EngFreeMem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-base-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngFreeMem
---

# EngFreeMem macro


## -description

The <b>EngFreeMem</b> function deallocates a block of system memory.

## -parameters

### -param p [in]

Pointer to the block of memory being deallocated.

## -remarks

This routine releases memory allocated by <a href="/windows/desktop/api/winddi/nf-winddi-engallocmem">EngAllocMem</a>. The memory block must not be accessed after it is freed.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engallocmem">EngAllocMem</a>