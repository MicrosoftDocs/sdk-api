---
UID: NS:winddi._ENGSAFESEMAPHORE
title: ENGSAFESEMAPHORE (winddi.h)
description: The ENGSAFESEMAPHORE structure provides the driver with a thread-safe semaphore.
helpviewer_keywords: ["ENGSAFESEMAPHORE","ENGSAFESEMAPHORE structure [Display Devices]","display.engsafesemaphore","grstrcts_63b165c2-5032-4dcb-9039-562a38f24cc4.xml","winddi/ENGSAFESEMAPHORE"]
old-location: display\engsafesemaphore.htm
tech.root: display
ms.assetid: 225ca482-6a45-4726-b51b-57fa76b8c5b0
ms.date: 12/05/2018
ms.keywords: ENGSAFESEMAPHORE, ENGSAFESEMAPHORE structure [Display Devices], display.engsafesemaphore, grstrcts_63b165c2-5032-4dcb-9039-562a38f24cc4.xml, winddi/ENGSAFESEMAPHORE
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ENGSAFESEMAPHORE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ENGSAFESEMAPHORE
 - winddi/_ENGSAFESEMAPHORE
 - ENGSAFESEMAPHORE
 - winddi/ENGSAFESEMAPHORE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - ENGSAFESEMAPHORE
---

# ENGSAFESEMAPHORE structure


## -description

The ENGSAFESEMAPHORE structure provides the driver with a thread-safe semaphore.

## -struct-fields

### -field hsem

Handle to the semaphore.

### -field lCount

Specifies the reference count on the semaphore.

## -remarks

A safe semaphore is a wrapper that contains a handle to a semaphore and a reference count on that semaphore.

The driver allocates an ENGSAFESEMAPHORE structure and passes it to <a href="/windows/desktop/api/winddi/nf-winddi-enginitializesafesemaphore">EngInitializeSafeSemaphore</a> for initialization. GDI operates the safe semaphore under a lock and maintains a reference count on it, making it suitable for multithreading.

Once the safe semaphore is initialized, the driver can call <a href="/windows/desktop/api/winddi/nf-winddi-engacquiresemaphore">EngAcquireSemaphore</a> and <a href="/windows/desktop/api/winddi/nf-winddi-engreleasesemaphore">EngReleaseSemaphore</a> with the <b>hsem</b> for synchronization.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engacquiresemaphore">EngAcquireSemaphore</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engdeletesafesemaphore">EngDeleteSafeSemaphore</a>



<a href="/windows/desktop/api/winddi/nf-winddi-enginitializesafesemaphore">EngInitializeSafeSemaphore</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engreleasesemaphore">EngReleaseSemaphore</a>