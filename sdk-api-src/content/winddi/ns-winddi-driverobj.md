---
UID: NS:winddi._DRIVEROBJ
title: DRIVEROBJ (winddi.h)
description: The DRIVEROBJ structure is used to track a resource, allocated by a driver, that requires use GDI services.
helpviewer_keywords: ["DRIVEROBJ","DRIVEROBJ structure [Display Devices]","display.driverobj","grstrcts_8b5c3216-cbe0-4ddf-97b3-c54b39f996cb.xml","winddi/DRIVEROBJ"]
old-location: display\driverobj.htm
tech.root: display
ms.assetid: 313ee1bf-ee0c-4283-b5e1-5bbabb944a4a
ms.date: 12/05/2018
ms.keywords: DRIVEROBJ, DRIVEROBJ structure [Display Devices], display.driverobj, grstrcts_8b5c3216-cbe0-4ddf-97b3-c54b39f996cb.xml, winddi/DRIVEROBJ
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
req.typenames: DRIVEROBJ
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DRIVEROBJ
 - winddi/_DRIVEROBJ
 - DRIVEROBJ
 - winddi/DRIVEROBJ
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
 - DRIVEROBJ
---

# DRIVEROBJ structure


## -description

The DRIVEROBJ structure is used to track a resource, allocated by a driver, that requires use GDI services. A DRIVEROBJ structure allows a display driver to request the GDI service in managing per-process resources. By creating a DRIVEROBJ structure, a display driver can ensure that resources will be released when an application terminates.

## -struct-fields

### -field pvObj

Pointer to the driver resource that will be tracked by the DRIVEROBJ structure. The resource is associated with the current client process.

### -field pFreeProc

Pointer to a driver-supplied callback function that frees the resource pointed to by <b>pvObj</b>. This callback function has the following prototype:


```
BOOL (CALLBACK * FREEOBJPROC) (DRIVEROBJ * pDriverObj);
```


The callback function returns <b>TRUE</b> if it is able to free the resource, and <b>FALSE</b> otherwise.

### -field hdev

GDI handle to the physical device associated with the object.

### -field dhpdev

Pointer to the driver's private instance data; that is, this member identifies the driver's <a href="/windows-hardware/drivers/">PDEV</a>.

## -remarks

A DRIVEROBJ structure allows a display driver to request the GDI service in managing per-process resources. By creating a DRIVEROBJ structure, a display driver can ensure that resources will be released when an application terminates.

Some drivers, in their Escape support, allocate resources on behalf of applications. In such cases, the DRIVEROBJ structure provides a means for the application to notify the driver when it terminates. GDI will call the driver's cleanup function for each DRIVEROBJ structure allocated in an application's context that is not deleted before the application terminates.

This structure provides a locking mechanism for exclusive access to the associated resource.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engcreatedriverobj">EngCreateDriverObj</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engdeletedriverobj">EngDeleteDriverObj</a>



<a href="/windows/desktop/api/winddi/nf-winddi-englockdriverobj">EngLockDriverObj</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engunlockdriverobj">EngUnlockDriverObj</a>