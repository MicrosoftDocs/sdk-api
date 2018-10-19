---
UID: NS:winddi._DRIVEROBJ
title: "_DRIVEROBJ"
author: windows-sdk-content
description: The DRIVEROBJ structure is used to track a resource, allocated by a driver, that requires use GDI services.
old-location: display\driverobj.htm
tech.root: display
ms.assetid: 313ee1bf-ee0c-4283-b5e1-5bbabb944a4a
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: DRIVEROBJ, DRIVEROBJ structure [Display Devices], _DRIVEROBJ, display.driverobj, grstrcts_8b5c3216-cbe0-4ddf-97b3-c54b39f996cb.xml, winddi/DRIVEROBJ
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DRIVEROBJ
product: Windows
targetos: Windows
req.typenames: DRIVEROBJ
req.redist: 
---

# _DRIVEROBJ structure


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

Pointer to the driver's private instance data; that is, this member identifies the driver's <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a>.


## -remarks



A DRIVEROBJ structure allows a display driver to request the GDI service in managing per-process resources. By creating a DRIVEROBJ structure, a display driver can ensure that resources will be released when an application terminates.

Some drivers, in their Escape support, allocate resources on behalf of applications. In such cases, the DRIVEROBJ structure provides a means for the application to notify the driver when it terminates. GDI will call the driver's cleanup function for each DRIVEROBJ structure allocated in an application's context that is not deleted before the application terminates.

This structure provides a locking mechanism for exclusive access to the associated resource.




## -see-also




<a href="https://msdn.microsoft.com/2912a456-e5d7-4ae4-b8b0-d16c9e8eadf2">EngCreateDriverObj</a>



<a href="https://msdn.microsoft.com/5c4f7f6a-331e-4c5d-9663-6a84245a203f">EngDeleteDriverObj</a>



<a href="https://msdn.microsoft.com/9ed3142d-2b20-4453-9057-80e6f8f92ff2">EngLockDriverObj</a>



<a href="https://msdn.microsoft.com/027bf180-b226-4d88-803d-2839417f727f">EngUnlockDriverObj</a>
 

 

