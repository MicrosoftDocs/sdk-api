---
UID: NF:winddi.EngAcquireSemaphore
title: EngAcquireSemaphore function (winddi.h)
description: The EngAcquireSemaphore function acquires the resource associated with the semaphore for exclusive access by the calling thread.
helpviewer_keywords: ["EngAcquireSemaphore","EngAcquireSemaphore function [Display Devices]","display.engacquiresemaphore","gdifncs_eae93ab5-f0f0-4d4e-a857-50ec8698527b.xml","winddi/EngAcquireSemaphore"]
old-location: display\engacquiresemaphore.htm
tech.root: display
ms.assetid: da13ff30-7817-4ed4-9791-2d205a260259
ms.date: 12/05/2018
ms.keywords: EngAcquireSemaphore, EngAcquireSemaphore function [Display Devices], display.engacquiresemaphore, gdifncs_eae93ab5-f0f0-4d4e-a857-50ec8698527b.xml, winddi/EngAcquireSemaphore
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
 - EngAcquireSemaphore
 - winddi/EngAcquireSemaphore
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
 - EngAcquireSemaphore
---

# EngAcquireSemaphore function


## -description

The <b>EngAcquireSemaphore</b> function acquires the resource associated with the semaphore for exclusive access by the calling thread.

## -parameters

### -param hsem [in]

Handle to the semaphore associated with the resource to be acquired.

## -returns

None

## -remarks

<b>EngAcquireSemaphore</b> allows exclusive access to the driver resource associated with the semaphore by locking out all other threads from accessing the semaphore's resource.

A call to this routine should be followed with a call to <a href="/windows/desktop/api/winddi/nf-winddi-engreleasesemaphore">EngReleaseSemaphore</a> as quickly as possible.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engcreatesemaphore">EngCreateSemaphore</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engdeletesemaphore">EngDeleteSemaphore</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engissemaphoreowned">EngIsSemaphoreOwned</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engissemaphoreownedbycurrentthread">EngIsSemaphoreOwnedByCurrentThread</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engreleasesemaphore">EngReleaseSemaphore</a>