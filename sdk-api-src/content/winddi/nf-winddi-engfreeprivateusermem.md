---
UID: NF:winddi.EngFreePrivateUserMem
title: EngFreePrivateUserMem macro (winddi.h)
description: The EngFreePrivateUserMem function deallocates a block of private user memory.
helpviewer_keywords: ["EngFreePrivateUserMem","EngFreePrivateUserMem function [Display Devices]","display.engfreeprivateusermem","gdifncs_debf1b76-d783-4b91-832e-c95c2c41af76.xml","winddi/EngFreePrivateUserMem"]
old-location: display\engfreeprivateusermem.htm
tech.root: display
ms.assetid: 098bba48-849e-4a35-801c-9573bc5c33f5
ms.date: 12/05/2018
ms.keywords: EngFreePrivateUserMem, EngFreePrivateUserMem function [Display Devices], display.engfreeprivateusermem, gdifncs_debf1b76-d783-4b91-832e-c95c2c41af76.xml, winddi/EngFreePrivateUserMem
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
 - EngFreePrivateUserMem
 - winddi/EngFreePrivateUserMem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngFreePrivateUserMem
---

# EngFreePrivateUserMem macro


## -description

The <b>EngFreePrivateUserMem</b> function deallocates a block of private user memory.

## -parameters

### -param psl [in]

Pointer to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure representing the DirectDraw surface with which the memory is associated.

### -param p [in]

Pointer to the block of user memory being deallocated.

## -remarks

This routine deallocates a block of memory allocated by <a href="/windows/desktop/api/winddi/nf-winddi-engallocprivateusermem">EngAllocPrivateUserMem</a>.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engallocprivateusermem">EngAllocPrivateUserMem</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engallocusermem">EngAllocUserMem</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engfreeusermem">EngFreeUserMem</a>