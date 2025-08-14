---
UID: NF:winddi.EngCreateDriverObj
title: EngCreateDriverObj function (winddi.h)
description: The EngCreateDriverObj function creates a DRIVEROBJ structure.
helpviewer_keywords: ["EngCreateDriverObj","EngCreateDriverObj function [Display Devices]","display.engcreatedriverobj","gdifncs_b2ab33cf-bcdf-418d-87a5-eee4b0704433.xml","winddi/EngCreateDriverObj"]
old-location: display\engcreatedriverobj.htm
tech.root: display
ms.assetid: 2912a456-e5d7-4ae4-b8b0-d16c9e8eadf2
ms.date: 12/05/2018
ms.keywords: EngCreateDriverObj, EngCreateDriverObj function [Display Devices], display.engcreatedriverobj, gdifncs_b2ab33cf-bcdf-418d-87a5-eee4b0704433.xml, winddi/EngCreateDriverObj
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
 - EngCreateDriverObj
 - winddi/EngCreateDriverObj
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
 - EngCreateDriverObj
---

# EngCreateDriverObj function


## -description

The <b>EngCreateDriverObj</b> function creates a <a href="/windows/desktop/api/winddi/ns-winddi-driverobj">DRIVEROBJ</a> structure.

## -parameters

### -param pvObj

Pointer to the driver resource that will be tracked by the DRIVEROBJ structure. The resource is associated with the current client process.

### -param pFreeObjProc

Pointer to a driver-supplied callback function that frees the resource pointed to by <i>pvObj</i>. The callback function should be defined as follows, where <i>pDriverObj</i> points to the DRIVEROBJ structure:


```
BOOL CALLBACK DrvobjFreeObjProc(DRIVEROBJ *pDriverObj);
```

### -param hdev

Handle to the physical device associated with the object. This parameter is the GDI handle received by the driver's <a href="/windows/desktop/api/winddi/nf-winddi-drvcompletepdev">DrvCompletePDEV</a> function.

## -returns

The return value is a handle that identifies the newly-created DRIVEROBJ structure if the function is successful. Otherwise, it is zero.

## -remarks

This structure is used to track a device-managed resource that must be released if the resource-allocating process terminates without first cleaning it up.

The driver can explicitly delete the DRIVEROBJ structure by calling <a href="/windows/desktop/api/winddi/nf-winddi-engdeletedriverobj">EngDeleteDriverObj</a>. Otherwise, the engine frees the resource by calling the function pointed to by <i>pFreeObjProc</i> when the process that created the DRIVEROBJ terminates.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-driverobj">DRIVEROBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engdeletedriverobj">EngDeleteDriverObj</a>