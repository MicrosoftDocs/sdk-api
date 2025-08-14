---
UID: NF:winddi.EngReleaseSemaphore
title: EngReleaseSemaphore function (winddi.h)
description: The EngReleaseSemaphore function releases the specified semaphore.
helpviewer_keywords: ["EngReleaseSemaphore","EngReleaseSemaphore function [Display Devices]","display.engreleasesemaphore","gdifncs_e4181ebe-43c7-4a59-8f19-e1c37f89524b.xml","winddi/EngReleaseSemaphore"]
old-location: display\engreleasesemaphore.htm
tech.root: display
ms.assetid: e89a556f-4071-425b-b138-bfb7b49a5e8c
ms.date: 12/05/2018
ms.keywords: EngReleaseSemaphore, EngReleaseSemaphore function [Display Devices], display.engreleasesemaphore, gdifncs_e4181ebe-43c7-4a59-8f19-e1c37f89524b.xml, winddi/EngReleaseSemaphore
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
 - EngReleaseSemaphore
 - winddi/EngReleaseSemaphore
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
 - EngReleaseSemaphore
---

# EngReleaseSemaphore function


## -description

The <b>EngReleaseSemaphore</b> function releases the specified semaphore.

## -parameters

### -param hsem [in]

Handle to the semaphore to be released.

## -returns

None

## -remarks

<b>EngReleaseSemaphore</b> releases the semaphore's exclusive lock on a driver's resource and reenables the delivery of special kernel asynchronous procedure calls.

The lock and asynchronous procedure call suspension were acquired in a call to <a href="/windows/desktop/api/winddi/nf-winddi-engacquiresemaphore">EngAcquireSemaphore</a>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engacquiresemaphore">EngAcquireSemaphore</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engdeletesemaphore">EngDeleteSemaphore</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engissemaphoreowned">EngIsSemaphoreOwned</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engissemaphoreownedbycurrentthread">EngIsSemaphoreOwnedByCurrentThread</a>