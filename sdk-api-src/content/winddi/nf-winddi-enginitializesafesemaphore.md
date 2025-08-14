---
UID: NF:winddi.EngInitializeSafeSemaphore
title: EngInitializeSafeSemaphore function (winddi.h)
description: The EngInitializeSafeSemaphore function initializes the specified safe semaphore.
helpviewer_keywords: ["EngInitializeSafeSemaphore","EngInitializeSafeSemaphore function [Display Devices]","display.enginitializesafesemaphore","gdifncs_92f07217-a6d2-4996-99a9-eb289a713e19.xml","winddi/EngInitializeSafeSemaphore"]
old-location: display\enginitializesafesemaphore.htm
tech.root: display
ms.assetid: 17b614b0-1c41-442c-b787-978eac3ade45
ms.date: 12/05/2018
ms.keywords: EngInitializeSafeSemaphore, EngInitializeSafeSemaphore function [Display Devices], display.enginitializesafesemaphore, gdifncs_92f07217-a6d2-4996-99a9-eb289a713e19.xml, winddi/EngInitializeSafeSemaphore
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
 - EngInitializeSafeSemaphore
 - winddi/EngInitializeSafeSemaphore
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
 - EngInitializeSafeSemaphore
---

# EngInitializeSafeSemaphore function


## -description

The <b>EngInitializeSafeSemaphore</b> function initializes the specified safe semaphore.

## -parameters

### -param pssem [out]

Pointer to the driver-allocated <a href="/windows/desktop/api/winddi/ns-winddi-engsafesemaphore">ENGSAFESEMAPHORE</a> structure to be initialized.

## -returns

<b>EngInitializeSafeSemaphore</b> returns <b>TRUE</b> upon success. Otherwise, it returns <b>FALSE</b>.

## -remarks

<b>EngInitializeSafeSemaphore</b> and <a href="/windows/desktop/api/winddi/nf-winddi-engdeletesafesemaphore">EngDeleteSafeSemaphore</a> are thread-safe, operating under a lock and maintaining a reference count on the semaphore. This guarantees that only one semaphore is created regardless of the number of simultaneous calls to it, and that the semaphore exists until the last reference to it is released.

Once the safe semaphore is initialized, the driver can call <a href="/windows/desktop/api/winddi/nf-winddi-engacquiresemaphore">EngAcquireSemaphore</a> and <a href="/windows/desktop/api/winddi/nf-winddi-engreleasesemaphore">EngReleaseSemaphore</a> with the <b>hsem</b> member of the <a href="/windows/desktop/api/winddi/ns-winddi-engsafesemaphore">ENGSAFESEMAPHORE</a> structure for synchronization.

Callers of <b>EngInitializeSafeSemaphore</b> should call <b>EngDeleteSafeSemaphore</b> when they no longer need the semaphore.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-engsafesemaphore">ENGSAFESEMAPHORE</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engacquiresemaphore">EngAcquireSemaphore</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engdeletesafesemaphore">EngDeleteSafeSemaphore</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engissemaphoreowned">EngIsSemaphoreOwned</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engissemaphoreownedbycurrentthread">EngIsSemaphoreOwnedByCurrentThread</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engreleasesemaphore">EngReleaseSemaphore</a>