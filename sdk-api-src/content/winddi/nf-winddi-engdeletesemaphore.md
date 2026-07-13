---
UID: NF:winddi.EngDeleteSemaphore
title: EngDeleteSemaphore function (winddi.h)
description: The EngDeleteSemaphore function deletes a semaphore object from the system's resource list.
helpviewer_keywords: ["EngDeleteSemaphore","EngDeleteSemaphore function [Display Devices]","display.engdeletesemaphore","gdifncs_a669ceb3-f9b3-4940-b1f8-17c55ee42f59.xml","winddi/EngDeleteSemaphore"]
old-location: display\engdeletesemaphore.htm
tech.root: display
ms.assetid: 6855017c-8919-496b-b82c-d65dea7ad5f0
ms.date: 12/05/2018
ms.keywords: EngDeleteSemaphore, EngDeleteSemaphore function [Display Devices], display.engdeletesemaphore, gdifncs_a669ceb3-f9b3-4940-b1f8-17c55ee42f59.xml, winddi/EngDeleteSemaphore
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
 - EngDeleteSemaphore
 - winddi/EngDeleteSemaphore
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - EngDeleteSemaphore
---

# EngDeleteSemaphore function


## -description

The <b>EngDeleteSemaphore</b> function deletes a semaphore object from the system's resource list.

## -parameters

### -param hsem [in]

Handle to the semaphore to be deleted. The semaphore was created in <a href="/windows/desktop/api/winddi/nf-winddi-engcreatesemaphore">EngCreateSemaphore</a>.

## -returns

None

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engacquiresemaphore">EngAcquireSemaphore</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engcreatesemaphore">EngCreateSemaphore</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engreleasesemaphore">EngReleaseSemaphore</a>