---
UID: NF:winddi.EngFreeUserMem
title: EngFreeUserMem macro (winddi.h)
description: The EngFreeUserMem function deallocates a block of user memory.
helpviewer_keywords: ["EngFreeUserMem","EngFreeUserMem function [Display Devices]","display.engfreeusermem","gdifncs_954f4161-3780-41ac-9a53-fa60051cc637.xml","winddi/EngFreeUserMem"]
old-location: display\engfreeusermem.htm
tech.root: display
ms.assetid: 3d409288-697e-4fa7-8ca9-ae80335f48a2
ms.date: 12/05/2018
ms.keywords: EngFreeUserMem, EngFreeUserMem function [Display Devices], display.engfreeusermem, gdifncs_954f4161-3780-41ac-9a53-fa60051cc637.xml, winddi/EngFreeUserMem
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
 - EngFreeUserMem
 - winddi/EngFreeUserMem
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
 - EngFreeUserMem
---

# EngFreeUserMem macro


## -description

The <b>EngFreeUserMem</b> function deallocates a block of user memory.

## -parameters

### -param p [in]

Pointer to the block of user memory being deallocated.

## -remarks

This routine releases memory allocated by <a href="/windows/desktop/api/winddi/nf-winddi-engallocusermem">EngAllocUserMem</a>. The memory block must not be accessed after it is freed.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engallocusermem">EngAllocUserMem</a>